<a href="../index.html" class="link-a079aa82--primary-53a25e66--logoLink-10d08504"></a>

<img src="https://gblobscdn.gitbook.com/orgs%2F-LxuH0qSm4xO9nWfEBlB%2Favatar.png?alt=media" class="image-67b14f24--avatar-1c1d03ec" />

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1--spaceNameText-677c2969">Everything curl</span>

<a href="../index.html" class="link-a079aa82--primary-53a25e66--logoLink-10d08504"></a>

<img src="https://gblobscdn.gitbook.com/orgs%2F-LxuH0qSm4xO9nWfEBlB%2Favatar.png?alt=media" class="image-67b14f24--avatar-1c1d03ec" />

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1--spaceNameText-677c2969">Everything curl</span>

<a href="../index.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Introduction</span></a>

<a href="../how-to-read.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">How to read this book</span></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">The cURL project</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Get curl</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Open Source</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">The source code</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Network and protocols</span>

<a href="network.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Networking simplified</span></a>

<a href="protocols.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Protocols</span></a>

<a href="curl.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">curl protocols</span></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Command line basics</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Using curl</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">How to HTTP with curl</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">libcurl basics</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP with libcurl</span>

<a href="../bindings.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Bindings</span></a>

<a href="../internals.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">libcurl internals</span></a>

<a href="../bookindex.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Index</span></a>

<a href="https://www.gitbook.com/?utm_source=content&amp;utm_medium=trademark&amp;utm_campaign=curl-1" class="reset-3c756112--trademark-a8da4b94"></a>

<span class="text-4505230f--TextH200-a3425406--textUIFamily-5ebd8e40">Powered by **GitBook**</span>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Networking simplified</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2"></span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2"></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="8bc69d1033dc4c19a06a23a2e7dc2414"><span data-offset-key="8bc69d1033dc4c19a06a23a2e7dc2414:0">Networking means communicating between two endpoints on the Internet. The Internet is just a bunch of interconnected machines (computers really), each using their own private addresses (called </span></span><a href="https://en.wikipedia.org/wiki/IP_address" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="9fcb73eed4f74b6280886b2f57da20dc"><span data-offset-key="9fcb73eed4f74b6280886b2f57da20dc:0">IP addresses</span></span></a><span data-key="114a107381e44561bdb79b4ebec7b0b7"><span data-offset-key="114a107381e44561bdb79b4ebec7b0b7:0">). The addresses each machine have can be of different types and machines can even have temporary addresses. These computers are often called hosts.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="d0e8914399c04e4b99e1d8e15a4d1c18"><span data-offset-key="d0e8914399c04e4b99e1d8e15a4d1c18:0">The computer, tablet or phone you sit in front of is usually called "the client" and the machine out there somewhere that you want to exchange data with is called "the server". The main difference between the client and the server is in the roles they play here. There's nothing that prevents the roles from being reversed in a subsequent operation.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="e8561fdd6b6b4ed4ab47e2840ad2d8aa"><span data-offset-key="e8561fdd6b6b4ed4ab47e2840ad2d8aa:0">Which machine</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="9909a8feb3cb4cfda5c9b32e9c5dcb1b"><span data-offset-key="9909a8feb3cb4cfda5c9b32e9c5dcb1b:0">When you want to initiate a transfer to one of the machines out there (a server), you usually do not know its IP addresses but instead you usually know its name. The name of the machine you will talk to is embedded in the URL that you work with when you use curl.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="0f229248431d4d3792746f626595fe64"><span data-offset-key="0f229248431d4d3792746f626595fe64:0">You might use a URL like "</span></span><a href="http://example.com/index.html" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="980cdce7674645aa8d615c549c59a6a4"><span data-offset-key="980cdce7674645aa8d615c549c59a6a4:0">http://example.com/index.html</span></span></a><span data-key="5362cd3fb2bb49cc92e603bd70518d67"><span data-offset-key="5362cd3fb2bb49cc92e603bd70518d67:0">", which means you will connect to and communicate with the host named example.com.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="d76641294f1c422ab4fe5c9a42193487"><span data-offset-key="d76641294f1c422ab4fe5c9a42193487:0">Host name resolving</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="1cb804b8fb8f49caad629208e7f43d1e"><span data-offset-key="1cb804b8fb8f49caad629208e7f43d1e:0">Once we know the host name, we need to figure out which IP addresses that host has so that we can contact it.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="cf2844494adc477f8204645cfb2609f1"><span data-offset-key="cf2844494adc477f8204645cfb2609f1:0">Converting the name to an IP address is often called 'name resolving'. The name is "resolved" to one or a set of addresses. This is usually done by a "DNS server", DNS being like a big lookup table that can convert names to addresses—all the names on the Internet, really. Your computer normally already knows the address of a computer that runs the DNS server as that is part of setting up the network.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="003c82fe1c96416e9efea1531dbf53ee"><span data-offset-key="003c82fe1c96416e9efea1531dbf53ee:0">curl will therefore ask the DNS server: "Hello, please give me all the addresses for example.com", and the server responds with a list of them. Or in the case you spell the name wrong, it can answer back that the name does not exist.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="3e2f1695dfb34008a13cc991d8a49c31"><span data-offset-key="3e2f1695dfb34008a13cc991d8a49c31:0">Establish a connection</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="1fc918de7b3b4b7fbc6f95bc9ab5981a"><span data-offset-key="1fc918de7b3b4b7fbc6f95bc9ab5981a:0">With a list of IP addresses for the host curl wants to contact, curl sends out a "connect request". The connection curl wants to establish is called TCP (</span></span><a href="https://en.wikipedia.org/wiki/Transmission_Control_Protocol" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="dbe11bb1b01844339ce92ca48aa460ea"><span data-offset-key="dbe11bb1b01844339ce92ca48aa460ea:0">Transmission Control Protocol</span></span></a><span data-key="1d02ff9ddbf74ba19049e10e918df612"><span data-offset-key="1d02ff9ddbf74ba19049e10e918df612:0">) and it works similar to connecting an invisible string between two computers. Once established, it can be used to send a stream of data in both directions.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="fdccb29af1764cd4a60dd60e5d10eb4f"><span data-offset-key="fdccb29af1764cd4a60dd60e5d10eb4f:0">As curl gets a list of addresses for the host, it will actually traverse that list of addresses when connecting and in case one fails it will try to connect to the next one until either one works or they all fail.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="c4ab226bd1564890a2f696d096008aea"><span data-offset-key="c4ab226bd1564890a2f696d096008aea:0">Connects to "port numbers"</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="eebacf8867f84d95a5b93227c8a34981"><span data-offset-key="eebacf8867f84d95a5b93227c8a34981:0">When connecting with TCP to a remote server, a client selects which port number to do that on. A port number is just a dedicated place for a particular service, which allows that same server to listen to other services on other port numbers at the same time.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="8cedb4c5ab1b4d99a071ab840c53879f"><span data-offset-key="8cedb4c5ab1b4d99a071ab840c53879f:0">Most common protocols have default port numbers that clients and servers use. For example, when using the "</span></span><a href="http://example.com/index.html" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="537d07fd2364433ab8ebf1d9a2df1a78"><span data-offset-key="537d07fd2364433ab8ebf1d9a2df1a78:0">http://example.com/index.html</span></span></a><span data-key="0c6e9e6663a54d7bb6d1d26b44d9a3e6"><span data-offset-key="0c6e9e6663a54d7bb6d1d26b44d9a3e6:0">" URL, that URL specifies a scheme called "http" which tells the client that it should try TCP port number 80 on the server by default. The URL can optionally provide another, custom, port number but if nothing special is specified, it will use the default port for the scheme used in the URL.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="0ea7fc6f85af4b3eb795568eb2ebe64d"><span data-offset-key="0ea7fc6f85af4b3eb795568eb2ebe64d:0">TLS</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="78a2cef492b24944a0356ff2412a5527"><span data-offset-key="78a2cef492b24944a0356ff2412a5527:0">After the TCP connection has been established, many transfers will require that both sides negotiate a better security level before continuing, and that is often TLS; Transport Layer Security. If that is used, the client and server will do a TLS handshake first and only continue further if that succeeds.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="e637239fe7ad4c13aebf3cac032d2d14"><span data-offset-key="e637239fe7ad4c13aebf3cac032d2d14:0">Transfer data</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="d861a11846c64a9ea4834f30b8539322"><span data-offset-key="d861a11846c64a9ea4834f30b8539322:0">When the connecting "string" we call TCP is attached to the remote computer (and we have done the possible additional TLS handshake), there's an established connection between the two machines and that connection can then be used to exchange data. That communication is done using a "protocol", as discussed in the following chapter.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="40ccb49832d04a928319bf5f7735ee52"><span data-offset-key="40ccb49832d04a928319bf5f7735ee52:0">Traditionally, what is called a </span><span data-offset-key="40ccb49832d04a928319bf5f7735ee52:1">_download_</span><span data-offset-key="40ccb49832d04a928319bf5f7735ee52:2"> is when data is transferred from a server to a client and inversely an </span><span data-offset-key="40ccb49832d04a928319bf5f7735ee52:3">_upload_</span><span data-offset-key="40ccb49832d04a928319bf5f7735ee52:4"> is when data is transferred from the client to the server. The client is down here. The server is up there.</span></span></span>

<a href="../protocols.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674"></a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Network and protocols</span>

<a href="protocols.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42"></a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Next</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Protocols</span>

<img src="https://avatars.githubusercontent.com/u/66654881?v=4" class="image-67b14f24--avatar-1c1d03ec" />

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 8 months ago</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40">Export as PDF</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="network.html#which-machine" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Which machine</span></span>

<a href="network.html#host-name-resolving" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Host name resolving</span></span>

<a href="network.html#establish-a-connection" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Establish a connection</span></span>

<a href="network.html#connects-to-port-numbers" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Connects to "port numbers"</span></span>

<a href="network.html#tls" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">TLS</span></span>

<a href="network.html#transfer-data" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Transfer data</span></span>
