<a href="bindings.html" class="navButton-94f2579c--navButtonClickable-161b88ca">

</a>

<a href="internals.html" class="navButton-94f2579c--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

</a>

<a href="bookindex.html" class="navButton-94f2579c--navButtonClickable-161b88ca">

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">libcurl internals</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="5d7648b26eb74c9880b588ebc9708a93">

<span data-offset-key="5d7648b26eb74c9880b588ebc9708a93:0">libcurl is never finished and is not just an off-the-shelf product. It is a living project that is improved and modified on almost a daily basis. We depend on skilled and interested hackers to fix bugs and to add features.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f635209a571a424aa0722d0f1a8c0453">

<span data-offset-key="f635209a571a424aa0722d0f1a8c0453:0">This chapter is meant to describe internal details to aid keen libcurl hackers to learn some basic concepts on how libcurl works internally and thus possibly where to look for problems or where to add things when you want to make the library do something new.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="0f97d8a29dba4ab8aede5702ca8c50f5">

<span data-offset-key="0f97d8a29dba4ab8aede5702ca8c50f5:0">Easy handle and connections</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="33ec46a77d4641b0bd6ec112423f758f">

<span data-offset-key="33ec46a77d4641b0bd6ec112423f758f:0">When reading the source code there are some useful basics that are good to know and keep in mind:</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="5dfd32f3986b4d3ebcab44b39d43d801">

<span data-offset-key="5dfd32f3986b4d3ebcab44b39d43d801:0">'data' is the variable name we use all over to refer to the easy handle (</span>

<span data-offset-key="5dfd32f3986b4d3ebcab44b39d43d801:1">`struct Curl_easy`</span>

<span data-offset-key="5dfd32f3986b4d3ebcab44b39d43d801:2">) for the transfer being worked on. No other name should be used for this and nothing else should use this name.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c872ce9980b14fefb1260e79591fb1c5">

<span data-offset-key="c872ce9980b14fefb1260e79591fb1c5:0">`conn`</span>

<span data-offset-key="c872ce9980b14fefb1260e79591fb1c5:1"> is the variable name we use all over the internals to refer to the current </span>

<span data-offset-key="c872ce9980b14fefb1260e79591fb1c5:2">_connection_</span>

<span data-offset-key="c872ce9980b14fefb1260e79591fb1c5:3"> the code works on (</span>

<span data-offset-key="c872ce9980b14fefb1260e79591fb1c5:4">`struct connectdata`</span>

<span data-offset-key="c872ce9980b14fefb1260e79591fb1c5:5">). A transfer typically uses a connection at some point and typically only one at a time. There's a </span>

<span data-offset-key="c872ce9980b14fefb1260e79591fb1c5:6">`conn->data`</span>

<span data-offset-key="c872ce9980b14fefb1260e79591fb1c5:7"> pointer that identifies the transfer that is currently working on this connection. A single connection can be reused over time by several transfers (and thus easy handles) and a single connection can also be used by several easy handles simultaneously when multiplexed connections are used. When muliplexing are used, the </span>

<span data-offset-key="c872ce9980b14fefb1260e79591fb1c5:8">`conn->data`</span>

<span data-offset-key="c872ce9980b14fefb1260e79591fb1c5:9"> pointer has to be updated accordingly quite frequently.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e37a3acff8f24a13ab90cbd49786a34d">

<span data-offset-key="e37a3acff8f24a13ab90cbd49786a34d:0">`result`</span>

<span data-offset-key="e37a3acff8f24a13ab90cbd49786a34d:1"> is the usual name we use for a </span>

<span data-offset-key="e37a3acff8f24a13ab90cbd49786a34d:2">`CURLcode`</span>

<span data-offset-key="e37a3acff8f24a13ab90cbd49786a34d:3"> variable to hold the return values from functions and if that return value is different than zero, it is an error and the function should clean up and return (usually passing on the same error code to its parent function).</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="101ce646be2e417294b703a023d3b643">

<span data-offset-key="101ce646be2e417294b703a023d3b643:0">Everything is multi</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="87d3964c0b1c4f6a8154fc2418951efc">

<span data-offset-key="87d3964c0b1c4f6a8154fc2418951efc:0">libcurl offers a few different APIs to do transfers; where the primary differences are the synchronous easy interface versus the non-blocking multi interface. The multi interface itself can then be further used either by using the event-driven socket interface or the "normal" perform interface.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="fded7d27c50c43e2a2e3f1301a27ca28">

<span data-offset-key="fded7d27c50c43e2a2e3f1301a27ca28:0">Internally however, everything is written for the event-driven interface. Everything needs to be written in non-blocking fashion so that functions are never waiting for data in loop or similar. Unless they are the "surface" functions that have that expressed functionality.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="27a3664acba44f02933a006350122a17">

<span data-offset-key="27a3664acba44f02933a006350122a17:0">The function </span>

<span data-offset-key="27a3664acba44f02933a006350122a17:1">`curl_easy_perform()`</span>

<span data-offset-key="27a3664acba44f02933a006350122a17:2"> which performs a single transfer synchronously, is itself just a wrapper function that internally will setup and use the multi interface itself.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="7251f9d125b04ab781766e8c11dca669">

<span data-offset-key="7251f9d125b04ab781766e8c11dca669:0">Everything is state machines</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8a845572b2d8403b8a525866ee698838">

<span data-offset-key="8a845572b2d8403b8a525866ee698838:0">To facilitate that non-blocking nature, the curl source is full of state machines. Work on as much data as there is and drive the state machine to where it can go based on what's available and allow the functions to continue from that point later on when more data arrives that then might drive the state machine further.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="41fb413d914d4f55aeb0937e2af942f4">

<span data-offset-key="41fb413d914d4f55aeb0937e2af942f4:0">There are such states in many different levels for a given transfer and the code for each particular protocol may have its own set of state machines.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9df38b90c6c948009a3529938209504e">

<span data-offset-key="9df38b90c6c948009a3529938209504e:0">One of the primary states is the main transfer "mode" the easy handle holds, which says if the current transfer is resolving, waiting for a resolve, connecting, waiting for a connect, issuing a request, doing a transfer etc (see the </span>

<span data-offset-key="9df38b90c6c948009a3529938209504e:1">`CURLMstate`</span>

<span data-offset-key="9df38b90c6c948009a3529938209504e:2"> enum in </span>

<span data-offset-key="9df38b90c6c948009a3529938209504e:3">`lib/multihandle.h`</span>

<span data-offset-key="9df38b90c6c948009a3529938209504e:4">). Every transfer done with libcurl has an associated easy handle and every easy handle will exercise that state machine.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="8d3931966c15413aaaefad52edb6b3a7">

<span data-offset-key="8d3931966c15413aaaefad52edb6b3a7:0">Different protocols "hooked in"</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="df454ae5c42d42c18d9b5ac4204ac33e">

<span data-offset-key="df454ae5c42d42c18d9b5ac4204ac33e:0">libcurl is a multi-protocol transfer library. The core of the code is a set of generic functions that are used for transfers in general and will mostly work the same for all protocols. The main state machine described above for example is there and works for all protocols - even though some protocols may not make use of all states for all transfers.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e84bbbbccca341a982fa6858bab43a9a">

<span data-offset-key="e84bbbbccca341a982fa6858bab43a9a:0">However, each different protocol libcurl speaks also has its unique particularities and specialties. In order to not have the code littered with conditions in the style "if the protocol is XYZ, then do...", we instead have the concept of </span>

<span data-offset-key="e84bbbbccca341a982fa6858bab43a9a:1">`Curl_handler`</span>

<span data-offset-key="e84bbbbccca341a982fa6858bab43a9a:2">. Each supported protocol defines one of those in </span>

<span data-offset-key="e84bbbbccca341a982fa6858bab43a9a:3">`lib/url.c`</span>

<span data-offset-key="e84bbbbccca341a982fa6858bab43a9a:4"> there's an array of pointers to such handlers called </span>

<span data-offset-key="e84bbbbccca341a982fa6858bab43a9a:5">`protocols[]`</span>

<span data-offset-key="e84bbbbccca341a982fa6858bab43a9a:6">.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="fd8ced848563491497542cf50b26f016">

<span data-offset-key="fd8ced848563491497542cf50b26f016:0">When a transfer is about to be done, libcurl parses the URL it is about to operate on and among other things it figures out what protocol to use. Normally this can be done by looking at the scheme part of the URL. For </span>

<span data-offset-key="fd8ced848563491497542cf50b26f016:1">`https://example.com`</span>

<span data-offset-key="fd8ced848563491497542cf50b26f016:2"> that is </span>

<span data-offset-key="fd8ced848563491497542cf50b26f016:3">`https`</span>

<span data-offset-key="fd8ced848563491497542cf50b26f016:4"> and for </span>

<span data-offset-key="fd8ced848563491497542cf50b26f016:5">`imaps://example.com`</span>

<span data-offset-key="fd8ced848563491497542cf50b26f016:6"> it is </span>

<span data-offset-key="fd8ced848563491497542cf50b26f016:7">`imaps`</span>

<span data-offset-key="fd8ced848563491497542cf50b26f016:8">. Using the provided scheme, libcurl sets the </span>

<span data-offset-key="fd8ced848563491497542cf50b26f016:9">`conn->handler`</span>

<span data-offset-key="fd8ced848563491497542cf50b26f016:10"> pointer to the handler struct for the protocol that handles this URL.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="cc8d0ee8a8ff43509e7e6701bb0f978f">

<span data-offset-key="cc8d0ee8a8ff43509e7e6701bb0f978f:0">The handler struct contains a set of function pointers that can be NULL or set to point to a protocol specific function to do things necessary for that protocol to work for a transfer. Things that not all other protocols need. The handler struct also sets up the name of the protocol and describes its feature set with a bitmask.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2ca08a4e54ce42ea8bbbf8890f5a313f">

<span data-offset-key="2ca08a4e54ce42ea8bbbf8890f5a313f:0">A libcurl transfer is built around a set of different "actions" and the handler can extend each of them. Here are some example function pointers in this struct and how they are used:</span>

</span>

</span>

<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="c7cccaa6a2ea483ea8bb108d88e7c884">

<span data-offset-key="c7cccaa6a2ea483ea8bb108d88e7c884:0">Setup connection</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4b8157a7d82f4d7ba524830b44a33596">

<span data-offset-key="4b8157a7d82f4d7ba524830b44a33596:0">If a connection cannot be reused for a transfer, it needs to setup a connection to the host given in the URL and when it does, it can also call the protocol handler's function for it. Like this:</span>

</span>

</span>    if(conn->handler->setup_connection)  result = conn->handler->setup_connection(conn);<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="449cd99fb04149feb66d775e51d2f599">

<span data-offset-key="449cd99fb04149feb66d775e51d2f599:0">Connect</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="61d47c3563664eeda6c8e1f4fdd3ad1f">

<span data-offset-key="61d47c3563664eeda6c8e1f4fdd3ad1f:0">After a connection has been established, this function gets called</span>

</span>

</span>    if(conn->handler->connect_it)  result = conn->handler->connect_it(conn, &done);<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="5459c6a0983f483790daafe82555eb8b">

<span data-offset-key="5459c6a0983f483790daafe82555eb8b:0">Do</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="13641f30a3d24a3487d7587f0a513923">

<span data-offset-key="13641f30a3d24a3487d7587f0a513923:0">"Do" is simply the action that issues a request for the particular resource the URL identifies. All protocol has a do action so this function must be provided:</span>

</span>

</span>    result = conn->handler->do_it(conn, &done);<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="7f404d8d68364e85ba7474bda491381a">

<span data-offset-key="7f404d8d68364e85ba7474bda491381a:0">Done</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9c4bb81afe404d098d417c5781fc7e2f">

<span data-offset-key="9c4bb81afe404d098d417c5781fc7e2f:0">When a transfer is completed, the "done" action is taken:</span>

</span>

</span>    result = conn->handler->done(conn);<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="f941ade7879c475aaaf4b0fe3ee83c18">

<span data-offset-key="f941ade7879c475aaaf4b0fe3ee83c18:0">Disconnect</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b13ae5950a9f4608896677cb4b8a39ab">

<span data-offset-key="b13ae5950a9f4608896677cb4b8a39ab:0">The connection is about to be taken down.</span>

</span>

</span>    result = conn->handler->disconnect(conn, dead_connection);<a href="bindings.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Bindings</span>

<a href="bookindex.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">

</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 12 months ago</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="internals.html#easy-handle-and-connections" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Easy handle and connections</span>

</span>

<a href="internals.html#everything-is-multi" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Everything is multi</span>

</span>

<a href="internals.html#everything-is-state-machines" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Everything is state machines</span>

</span>

<a href="internals.html#different-protocols-hooked-in" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Different protocols "hooked in"</span>

</span>

<a href="internals.html#setup-connection" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Setup connection</span>

</span>

<a href="internals.html#connect" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Connect</span>

</span>

<a href="internals.html#do" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Do</span>

</span>

<a href="internals.html#done" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Done</span>

</span>

<a href="internals.html#disconnect" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Disconnect</span>

</span>
