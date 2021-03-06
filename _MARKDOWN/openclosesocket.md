<a href="write.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Write data</span>

</a>

<a href="openclosesocket.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Opensocket and closesocket</span>

</a>

<a href="sshkey.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">SSH key</span>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Opensocket and closesocket</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="73b47cf12ab046a4b08ed3e208b0f8c4">

<span data-offset-key="73b47cf12ab046a4b08ed3e208b0f8c4:0">Occasionally you end up in a situation where you want your application to control with more precision exactly what socket libcurl will use for its operations. libcurl offers this pair of callbacks that replaces libcurl's own call to </span>

<span data-offset-key="73b47cf12ab046a4b08ed3e208b0f8c4:1">`socket()`</span>

<span data-offset-key="73b47cf12ab046a4b08ed3e208b0f8c4:2"> and the subsequent </span>

<span data-offset-key="73b47cf12ab046a4b08ed3e208b0f8c4:3">`close()`</span>

<span data-offset-key="73b47cf12ab046a4b08ed3e208b0f8c4:4"> of the same file descriptor.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="f4a1fc4378044a80ae55156bd4dc3a39">

<span data-offset-key="f4a1fc4378044a80ae55156bd4dc3a39:0">Provide a file descriptor</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e03319928b444e8eb1e46865eb3a9c0b">

<span data-offset-key="e03319928b444e8eb1e46865eb3a9c0b:0">By setting the </span>

<span data-offset-key="e03319928b444e8eb1e46865eb3a9c0b:1">`CURLOPT_OPENSOCKETFUNCTION`</span>

<span data-offset-key="e03319928b444e8eb1e46865eb3a9c0b:2"> callback, you can provide a custom function to return a file descriptor for libcurl to use:</span>

</span>

</span> curl_easy_setopt(handle, CURLOPT_OPENSOCKETFUNCTION, opensocket_callback);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a0dbb93454e3462aaed373ced4a4189d">

<span data-offset-key="a0dbb93454e3462aaed373ced4a4189d:0">The </span>

<span data-offset-key="a0dbb93454e3462aaed373ced4a4189d:1">`opensocket_callback`</span>

<span data-offset-key="a0dbb93454e3462aaed373ced4a4189d:2"> function must match this prototype:</span>

</span>

</span> curl_socket_t opensocket_callback(void *clientp, curlsocktype purpose, struct curl_sockaddr *address);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="fbe25eb061494e2887f1c29674137aad">

<span data-offset-key="fbe25eb061494e2887f1c29674137aad:0">The callback gets the </span>

<span data-offset-key="fbe25eb061494e2887f1c29674137aad:1">_clientp_</span>

<span data-offset-key="fbe25eb061494e2887f1c29674137aad:2"> as first argument, which is simply an opaque pointer you set with </span>

<span data-offset-key="fbe25eb061494e2887f1c29674137aad:3">`CURLOPT_OPENSOCKETDATA`</span>

<span data-offset-key="fbe25eb061494e2887f1c29674137aad:4">.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a860cd5387084752b622793eb3e80754">

<span data-offset-key="a860cd5387084752b622793eb3e80754:0">The other two arguments pass in data that identifies for what </span>

<span data-offset-key="a860cd5387084752b622793eb3e80754:1">_purpose_</span>

<span data-offset-key="a860cd5387084752b622793eb3e80754:2"> and </span>

<span data-offset-key="a860cd5387084752b622793eb3e80754:3">_address_</span>

<span data-offset-key="a860cd5387084752b622793eb3e80754:4"> the socket is to be used. The </span>

<span data-offset-key="a860cd5387084752b622793eb3e80754:5">_purpose_</span>

<span data-offset-key="a860cd5387084752b622793eb3e80754:6"> is a typedef with a value of </span>

<span data-offset-key="a860cd5387084752b622793eb3e80754:7">`CURLSOCKTYPE_IPCXN`</span>

<span data-offset-key="a860cd5387084752b622793eb3e80754:8"> or </span>

<span data-offset-key="a860cd5387084752b622793eb3e80754:9">`CURLSOCKTYPE_ACCEPT`</span>

<span data-offset-key="a860cd5387084752b622793eb3e80754:10">, identifying in which circumstance the socket is created. The "accept" case being when libcurl is used to accept an incoming FTP connection for when FTP active mode is used, and all other cases when libcurl creates a socket for its own outgoing connections the </span>

<span data-offset-key="a860cd5387084752b622793eb3e80754:11">_IPCXN_</span>

<span data-offset-key="a860cd5387084752b622793eb3e80754:12"> value is passed in.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c8e8f5e7ec644f74b58a46154fe56072">

<span data-offset-key="c8e8f5e7ec644f74b58a46154fe56072:0">The </span>

<span data-offset-key="c8e8f5e7ec644f74b58a46154fe56072:1">_address_</span>

<span data-offset-key="c8e8f5e7ec644f74b58a46154fe56072:2"> pointer points to a </span>

<span data-offset-key="c8e8f5e7ec644f74b58a46154fe56072:3">`struct curl_sockaddr`</span>

<span data-offset-key="c8e8f5e7ec644f74b58a46154fe56072:4"> that describes the IP address of the network destination for which this socket is created. Your callback can for example use this information to whitelist or blacklist specific addresses or address ranges.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b296832ad3ef4fb68cf8c447a6d12ed1">

<span data-offset-key="b296832ad3ef4fb68cf8c447a6d12ed1:0">The socketopen callback is also explicitly allowed to modify the target address in that struct, if you would like to offer some sort of network filter or translation layer.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="d5e49f26243344c29e37aa7e9505e6bf">

<span data-offset-key="d5e49f26243344c29e37aa7e9505e6bf:0">The callback should return a file descriptor or </span>

<span data-offset-key="d5e49f26243344c29e37aa7e9505e6bf:1">`CURL_SOCKET_BAD`</span>

<span data-offset-key="d5e49f26243344c29e37aa7e9505e6bf:2">, which then will cause an unrecoverable error within libcurl and it will eventually return </span>

<span data-offset-key="d5e49f26243344c29e37aa7e9505e6bf:3">`CURLE_COULDNT_CONNECT`</span>

<span data-offset-key="d5e49f26243344c29e37aa7e9505e6bf:4"> from its perform function.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="38d3bf706ee44a75a05ca341982339d5">

<span data-offset-key="38d3bf706ee44a75a05ca341982339d5:0">If you want to return a file descriptor that is </span>

<span data-offset-key="38d3bf706ee44a75a05ca341982339d5:1">_already connected_</span>

<span data-offset-key="38d3bf706ee44a75a05ca341982339d5:2"> to a server, then you must also set the </span>

</span>

<a href="sockopt.html" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="e57d66a5ed7d4a8085ae54dce30bde8e">

<span data-offset-key="e57d66a5ed7d4a8085ae54dce30bde8e:0">sockopt callback</span>

</span>

</a>

<span data-key="76c69f001a8045cea9b9b87916ac00a6">

<span data-offset-key="76c69f001a8045cea9b9b87916ac00a6:0"> and make sure that returns the correct return value.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="00d1476a762a4188a76a193d6b6a154d">

<span data-offset-key="00d1476a762a4188a76a193d6b6a154d:0">The </span>

<span data-offset-key="00d1476a762a4188a76a193d6b6a154d:1">`curl_sockaddress`</span>

<span data-offset-key="00d1476a762a4188a76a193d6b6a154d:2"> struct looks like this:</span>

</span>

</span> struct curl_sockaddr { int family; int socktype; int protocol; unsigned int addrlen; struct sockaddr addr;};<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="b5ac274226c5493f99c040ec27f1c037">

<span data-offset-key="b5ac274226c5493f99c040ec27f1c037:0">Socket close callback</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b95a642693cc49d6bbffccee4d7f41a0">

<span data-offset-key="b95a642693cc49d6bbffccee4d7f41a0:0">The corresponding callback to the open socket is of course the close socket. Usually when you provide a custom way to provide a file descriptor you want to provide your own cleanup version as well:</span>

</span>

</span> curl_easy_setopt(handle, CURLOPT_CLOSEOCKETFUNCTION, closesocket_callback);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="416a8dbe590546ba8abf2e09024956a8">

<span data-offset-key="416a8dbe590546ba8abf2e09024956a8:0">The </span>

<span data-offset-key="416a8dbe590546ba8abf2e09024956a8:1">`closesocket_callback`</span>

<span data-offset-key="416a8dbe590546ba8abf2e09024956a8:2"> function must match this prototype:</span>

</span>

</span> int closesocket_callback(void \*clientp, curl_socket_t item);<a href="conversions.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Network data conversion</span>

<a href="sshkey.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">SSH key</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 12 months ago</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="openclosesocket.html#provide-a-file-descriptor" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Provide a file descriptor</span>

</span>

<a href="openclosesocket.html#socket-close-callback" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Socket close callback</span>

</span>
