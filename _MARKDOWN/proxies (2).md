<a href="easyhandle.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Easy handle</span>

</a>

<a href="connectionreuse.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Connection reuse</span>

</a>

<a href="cleanup.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Cleanup</span>

</a>

<a href="names.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Name resolving</span>

</a>

<a href="proxies.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

</a>

<a href="getinfo.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Post transfer info</span>

</a>

<a href="sharing.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Share data between handles</span>

</a>

<a href="url.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">URL API</span>

</a>

<a href="api.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">API compatibility</span>

</a>

<a href="libcurl.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">--libcurl</span>

</a>

<a href="headers.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Header files</span>

</a>

<a href="globalinit.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Global initialization</span>

</a>

<a href="threading.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">multi-threading</span>

</a>

<a href="curlcode.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">CURLcode return codes</span>

</a>

<a href="verbose.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Verbose operations</span>

</a>

<a href="cplusplus.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">for C++ programmers</span>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Proxies</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4c026d218dcc445d8edd444b18f57aa1">

<span data-offset-key="4c026d218dcc445d8edd444b18f57aa1:0">A proxy in a network context is a middle man, a server in between you as a client and the remote server you want to communicate with. The client contacts the middle man which then goes on to contact the remote server for you.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="bf782fb713ca41b9a19d1e22c1aad813">

<span data-offset-key="bf782fb713ca41b9a19d1e22c1aad813:0">This style of proxy use is sometimes used by companies and organizations, in which case you are usually required to use them to reach the target server.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b4570456773843689433f57f025748b8">

<span data-offset-key="b4570456773843689433f57f025748b8:0">There are several different kinds of proxies and different protocols to use when communicating with a proxy, and libcurl supports a few of the most common proxy protocols. It is important to realize that the protocol used to the proxy is not necessarily the same protocol used to the remote server.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7eec1df01d8f4871bdf0f521dff12030">

<span data-offset-key="7eec1df01d8f4871bdf0f521dff12030:0">When setting up a transfer with libcurl you need to point out the server name and port number of the proxy. You may find that your favorite browsers can do this in slightly more advanced ways than libcurl can, and we will get into such details in later sections.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="b96bd6f07c31449db0b7ffde70f2b567">

<span data-offset-key="b96bd6f07c31449db0b7ffde70f2b567:0">Proxy types</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="d5039bdcb02347c4afffdad3e315e11c">

<span data-offset-key="d5039bdcb02347c4afffdad3e315e11c:0">libcurl supports the two major proxy types: SOCKS and HTTP proxies. More specifically, it supports both SOCKS4 and SOCKS5 with or without remote name lookup, as well as both HTTP and HTTPS to the local proxy.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b07ff4b462fd4a35a3cd9a2b214fe6bb">

<span data-offset-key="b07ff4b462fd4a35a3cd9a2b214fe6bb:0">The easiest way to specify which kind of proxy you are talking to is to set the scheme part of the proxy host name string (</span>

<span data-offset-key="b07ff4b462fd4a35a3cd9a2b214fe6bb:1">`CURLOPT_PROXY`</span>

<span data-offset-key="b07ff4b462fd4a35a3cd9a2b214fe6bb:2">) to match it:</span>

</span>

</span> socks4://proxy.example.com:12345/socks4a://proxy.example.com:12345/socks5://proxy.example.com:12345/socks5h://proxy.example.com:12345/http://proxy.example.com:12345/https://proxy.example.com:12345/<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2cda22bacfcc423aba4f00b85017b42b">

<span data-offset-key="2cda22bacfcc423aba4f00b85017b42b:0">`socks4`</span>

<span data-offset-key="2cda22bacfcc423aba4f00b85017b42b:1"> - means SOCKS4 with local name resolving</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0f8b63d5dd8c429fb4639f7e918019e5">

<span data-offset-key="0f8b63d5dd8c429fb4639f7e918019e5:0">`socks4a`</span>

<span data-offset-key="0f8b63d5dd8c429fb4639f7e918019e5:1"> - means SOCKS4 with proxy's name resolving</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b4df357ec35140b184b05fd73e217f2a">

<span data-offset-key="b4df357ec35140b184b05fd73e217f2a:0">`socks5`</span>

<span data-offset-key="b4df357ec35140b184b05fd73e217f2a:1"> - means SOCKS5 with local name resolving</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0c449a9a28b349e08234d2a7c6421bf3">

<span data-offset-key="0c449a9a28b349e08234d2a7c6421bf3:0">`socks5h`</span>

<span data-offset-key="0c449a9a28b349e08234d2a7c6421bf3:1"> - means SOCKS5 with proxy's name resolving</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="72d1cac0754242e39216436cc139cc4b">

<span data-offset-key="72d1cac0754242e39216436cc139cc4b:0">`http`</span>

<span data-offset-key="72d1cac0754242e39216436cc139cc4b:1"> - means HTTP, which always lets the proxy resolve names</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9400e31f44a04721a938c457990e7ff3">

<span data-offset-key="9400e31f44a04721a938c457990e7ff3:0">`https`</span>

<span data-offset-key="9400e31f44a04721a938c457990e7ff3:1"> - means HTTPS </span>

<span data-offset-key="9400e31f44a04721a938c457990e7ff3:2">**to the proxy**</span>

<span data-offset-key="9400e31f44a04721a938c457990e7ff3:3">, which always lets the proxy resolve names (Note that HTTPS proxy support was added recently, in curl 7.52.0, and it still only works with a subset of the TLS libraries: OpenSSL, GnuTLS and NSS.)</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8d88689c93244471aea356fc5921031f">

<span data-offset-key="8d88689c93244471aea356fc5921031f:0">You can also opt to set the type of the proxy with a separate option if you prefer to only set the host name, using </span>

<span data-offset-key="8d88689c93244471aea356fc5921031f:1">`CURLOPT_PROXYTYPE`</span>

<span data-offset-key="8d88689c93244471aea356fc5921031f:2">. Similarly, you can set the proxy port number to use with </span>

<span data-offset-key="8d88689c93244471aea356fc5921031f:3">`CURLOPT_PROXYPORT`</span>

<span data-offset-key="8d88689c93244471aea356fc5921031f:4">.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="86ebd1bc960e485b9c0c04d852749944">

<span data-offset-key="86ebd1bc960e485b9c0c04d852749944:0">Local or proxy name lookup</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c7a061f233a447fe94a255ca1880dae8">

<span data-offset-key="c7a061f233a447fe94a255ca1880dae8:0">In a section above you can see that different proxy setups allow the name resolving to be done by different parties involved in the transfer. You can in several cases either have the client resolve the server host name and pass on the IP address to the proxy to connect to - which of course assumes that the name lookup works accurately on the client system - or you can hand over the name to the proxy to have the proxy resolve the name; converting it to an IP address to connect to.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2ac30464e2d04ce8b96aba6f49026a29">

<span data-offset-key="2ac30464e2d04ce8b96aba6f49026a29:0">When you are using an HTTP or HTTPS proxy, you always give the name to the proxy to resolve.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="51f33bfd892d433fa72027c8de0457ac">

<span data-offset-key="51f33bfd892d433fa72027c8de0457ac:0">Which proxy?</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="63fd4d503f594808836c7f59cce80583">

<span data-offset-key="63fd4d503f594808836c7f59cce80583:0">If your network connection requires the use of a proxy to reach the destination, you must figure this out and tell libcurl to use the correct proxy. There is no support in libcurl to make it automatically figure out or detect a proxy.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="33a7e658d6214f7089a756dada4a9805">

<span data-offset-key="33a7e658d6214f7089a756dada4a9805:0">When using a browser, it is popular to provide the proxy with a PAC script or other means but none of those are recognized by libcurl.</span>

</span>

</span>

<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="28c25b3800a24f69bfb9bac931bc0a5c">

<span data-offset-key="28c25b3800a24f69bfb9bac931bc0a5c:0">Proxy environment variables</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a06130be49b14cccbc61270e751901be">

<span data-offset-key="a06130be49b14cccbc61270e751901be:0">If no proxy option has been set, libcurl will check for the existence of specially named environment variables before it performs its transfer to see if a proxy is requested to get used.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6a71fd9a6d6d42adb5e032de6ab7d6bc">

<span data-offset-key="6a71fd9a6d6d42adb5e032de6ab7d6bc:0">You can specify the proxy by setting a variable named </span>

<span data-offset-key="6a71fd9a6d6d42adb5e032de6ab7d6bc:1">`[scheme]_proxy`</span>

<span data-offset-key="6a71fd9a6d6d42adb5e032de6ab7d6bc:2"> to hold the proxy host name (the same way you would specify the host with </span>

<span data-offset-key="6a71fd9a6d6d42adb5e032de6ab7d6bc:3">`-x`</span>

<span data-offset-key="6a71fd9a6d6d42adb5e032de6ab7d6bc:4">). So if you want to tell curl to use a proxy when accessing a HTTP server, you set the 'http_proxy' environment variable. Like this:</span>

</span>

</span> http_proxy=http://proxy.example.com:80<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8aaf491d15b8483a8b13a2af2c97610e">

<span data-offset-key="8aaf491d15b8483a8b13a2af2c97610e:0">The proxy example above is for HTTP, but can of course also set </span>

<span data-offset-key="8aaf491d15b8483a8b13a2af2c97610e:1">`ftp_proxy`</span>

<span data-offset-key="8aaf491d15b8483a8b13a2af2c97610e:2">, </span>

<span data-offset-key="8aaf491d15b8483a8b13a2af2c97610e:3">`https_proxy`</span>

<span data-offset-key="8aaf491d15b8483a8b13a2af2c97610e:4">, and so on for the specific protocols you want to proxy. All these proxy environment variable names except http_proxy can also be specified in uppercase, like </span>

<span data-offset-key="8aaf491d15b8483a8b13a2af2c97610e:5">`HTTPS_PROXY`</span>

<span data-offset-key="8aaf491d15b8483a8b13a2af2c97610e:6">.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6eb1debf59e4484dac43145e09535bf3">

<span data-offset-key="6eb1debf59e4484dac43145e09535bf3:0">To set a single variable that controls </span>

<span data-offset-key="6eb1debf59e4484dac43145e09535bf3:1">_all_</span>

<span data-offset-key="6eb1debf59e4484dac43145e09535bf3:2"> protocols, the </span>

<span data-offset-key="6eb1debf59e4484dac43145e09535bf3:3">`ALL_PROXY`</span>

<span data-offset-key="6eb1debf59e4484dac43145e09535bf3:4"> exists. If a specific protocol variable one exists, such a one will take precedence.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9af38410f15d4490bbd48cabfd94be8b">

<span data-offset-key="9af38410f15d4490bbd48cabfd94be8b:0">When using environment variables to set a proxy, you could easily end up in a situation where one or a few host names should be excluded from going through the proxy. This can be done with the </span>

<span data-offset-key="9af38410f15d4490bbd48cabfd94be8b:1">`NO_PROXY`</span>

<span data-offset-key="9af38410f15d4490bbd48cabfd94be8b:2"> variable - or the corresponding </span>

<span data-offset-key="9af38410f15d4490bbd48cabfd94be8b:3">`CURLOPT_NOPROXY`</span>

<span data-offset-key="9af38410f15d4490bbd48cabfd94be8b:4"> libcurl option. Set that to a comma- separated list of host names that should not use a proxy when being accessed. You can set NO_PROXY to be a single asterisk ('\*') to match all hosts.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="cd4f5f79debd434986bf364642f54f96">

<span data-offset-key="cd4f5f79debd434986bf364642f54f96:0">HTTP proxy</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a08f02ba0b3b45dcb14b536cdda6d509">

<span data-offset-key="a08f02ba0b3b45dcb14b536cdda6d509:0">The HTTP protocol details exactly how a HTTP proxy should be used. Instead of sending the request to the actual remote server, the client (libcurl) instead asks the proxy for the specific resource. The connection to the HTTP proxy is made using plain unencrypted HTTP.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f8b63aec333f48c9a2c00cbe885b3f43">

<span data-offset-key="f8b63aec333f48c9a2c00cbe885b3f43:0">If a HTTPS resource is requested, libcurl will instead issue a </span>

<span data-offset-key="f8b63aec333f48c9a2c00cbe885b3f43:1">`CONNECT`</span>

<span data-offset-key="f8b63aec333f48c9a2c00cbe885b3f43:2"> request to the proxy. Such a request opens a tunnel through the proxy, where it passes data through without understanding it. This way, libcurl can establish a secure end-to-end TLS connection even when a HTTP proxy is present.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a7f5d13492c444109f0e96f5fec6cff6">

<span data-offset-key="a7f5d13492c444109f0e96f5fec6cff6:0">You </span>

<span data-offset-key="a7f5d13492c444109f0e96f5fec6cff6:1">_can_</span>

<span data-offset-key="a7f5d13492c444109f0e96f5fec6cff6:2"> proxy non-HTTP protocols over a HTTP proxy, but since this is mostly done by the CONNECT method to tunnel data through it requires that the proxy is configured to allow the client to connect to those other particular remote port numbers. Many HTTP proxies are setup to inhibit connections to other port numbers than 80 and 443.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="61df1982cc714fd28ffd784a09c0652a">

<span data-offset-key="61df1982cc714fd28ffd784a09c0652a:0">HTTPS proxy</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="684d227f1d8547218ba162f5f460919c">

<span data-offset-key="684d227f1d8547218ba162f5f460919c:0">A HTTPS proxy is similar to a HTTP proxy but allows the client to connect to it using a secure HTTPS connection. Since the proxy connection is separate from the connection to the remote site even in this situation, as HTTPS to the remote site will be tunnelled through the HTTPS connection to the proxy, libcurl provies a whole set of TLS options for the proxy connection that are separate from the connection to the remote host.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="1b7e33040f18450ca11cbde691fccd1c">

<span data-offset-key="1b7e33040f18450ca11cbde691fccd1c:0">For example, </span>

<span data-offset-key="1b7e33040f18450ca11cbde691fccd1c:1">`CURLOPT_PROXY_CAINFO`</span>

<span data-offset-key="1b7e33040f18450ca11cbde691fccd1c:2"> is the same functionality for the HTTPS proxy as </span>

<span data-offset-key="1b7e33040f18450ca11cbde691fccd1c:3">`CURLOPT_CAINFO`</span>

<span data-offset-key="1b7e33040f18450ca11cbde691fccd1c:4"> is for the remote host. </span>

<span data-offset-key="1b7e33040f18450ca11cbde691fccd1c:5">`CURLOPT_PROXY_SSL_VERIFYPEER`</span>

<span data-offset-key="1b7e33040f18450ca11cbde691fccd1c:6"> is the proxy version of </span>

<span data-offset-key="1b7e33040f18450ca11cbde691fccd1c:7">`CURLOPT_SSL_VERIFYPEER`</span>

<span data-offset-key="1b7e33040f18450ca11cbde691fccd1c:8"> and so on.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="3c1e35d424344b68a2b90dc1bcd32c8f">

<span data-offset-key="3c1e35d424344b68a2b90dc1bcd32c8f:0">HTTPS proxies are still today fairly unusual in organizations and companies.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="a53dca2c501046389a278383add2f1a9">

<span data-offset-key="a53dca2c501046389a278383add2f1a9:0">Proxy authentication</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="21424d72374a40adb33754170faa20b6">

<span data-offset-key="21424d72374a40adb33754170faa20b6:0">Authentication with a proxy means that you need to provide valid credentials in the handshake negotiation with the proxy itself. The proxy authentication is then in addition to and separate of the possible authentication or lack of authentication with the remote host.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9311cb3b8daf47e9a8f55f41df1aa4ce">

<span data-offset-key="9311cb3b8daf47e9a8f55f41df1aa4ce:0">libcurl supports authentication with HTTP, HTTPS and SOCKS5 proxies. The key option is then </span>

<span data-offset-key="9311cb3b8daf47e9a8f55f41df1aa4ce:1">`CURLOPT_PROXYUSERPWD`</span>

<span data-offset-key="9311cb3b8daf47e9a8f55f41df1aa4ce:2"> which sets the user name and password to use - unless you set it within the </span>

<span data-offset-key="9311cb3b8daf47e9a8f55f41df1aa4ce:3">`CURLOPT_PROXY`</span>

<span data-offset-key="9311cb3b8daf47e9a8f55f41df1aa4ce:4"> string.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="48cc70c72de54884a4e655fb1d67b6a6">

<span data-offset-key="48cc70c72de54884a4e655fb1d67b6a6:0">Proxy headers</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0ea399a811af4108b295039b711c1c52">

<span data-offset-key="0ea399a811af4108b295039b711c1c52:0">TBD</span>

</span>

</span>

<a href="names.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Name resolving</span>

<a href="getinfo.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Post transfer info</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 8 months ago</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="proxies.html#proxy-types" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Proxy types</span>

</span>

<a href="proxies.html#local-or-proxy-name-lookup" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Local or proxy name lookup</span>

</span>

<a href="proxies.html#which-proxy" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Which proxy?</span>

</span>

<a href="proxies.html#proxy-environment-variables" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Proxy environment variables</span>

</span>

<a href="proxies.html#http-proxy" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">HTTP proxy</span>

</span>

<a href="proxies.html#https-proxy" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">HTTPS proxy</span>

</span>

<a href="proxies.html#proxy-authentication" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Proxy authentication</span>

</span>

<a href="proxies.html#proxy-headers" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Proxy headers</span>

</span>
