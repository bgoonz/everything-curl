<a href="connections.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

</a>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Connections</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ad9f672eb8184c649bf197923cfef21c">

<span data-offset-key="ad9f672eb8184c649bf197923cfef21c:0">Most of the protocols you use with curl speak TCP. With TCP, a client such as curl must first figure out the IP address(es) of the host you want to communicate with, then connect to it. "Connecting to it" means performing a TCP protocol handshake.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="92289d175d5643029a7b7490b0856bda">

<span data-offset-key="92289d175d5643029a7b7490b0856bda:0">For ordinary command line usage, operating on a URL, these are details which are taken care of under the hood, and which you can mostly ignore. But at times you might find yourself wanting to tweak the specifics…</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="f1ef1f9fc24b49f39dec1311d28ff0a3">

<span data-offset-key="f1ef1f9fc24b49f39dec1311d28ff0a3:0">Name resolve tricks</span>

</span>

</span>

<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="589e15b72e714a4c8e0eaae2c6261043">

<span data-offset-key="589e15b72e714a4c8e0eaae2c6261043:0">Edit the hosts file</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="03c89f53649749ae8b01a47b9578bd62">

<span data-offset-key="03c89f53649749ae8b01a47b9578bd62:0">Maybe you want the command </span>

<span data-offset-key="03c89f53649749ae8b01a47b9578bd62:1">`curl http://example.com`</span>

<span data-offset-key="03c89f53649749ae8b01a47b9578bd62:2"> to connect to your local server instead of the actual server.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="dd4d1bf33bdb4079b70486c8adbc68b4">

<span data-offset-key="dd4d1bf33bdb4079b70486c8adbc68b4:0">You can normally and easily do that by editing your </span>

<span data-offset-key="dd4d1bf33bdb4079b70486c8adbc68b4:1">`hosts`</span>

<span data-offset-key="dd4d1bf33bdb4079b70486c8adbc68b4:2"> file (</span>

<span data-offset-key="dd4d1bf33bdb4079b70486c8adbc68b4:3">`/etc/hosts`</span>

<span data-offset-key="dd4d1bf33bdb4079b70486c8adbc68b4:4"> on Linux and Unix-like systems) and adding, for example, </span>

<span data-offset-key="dd4d1bf33bdb4079b70486c8adbc68b4:5">`127.0.0.1 example.com`</span>

<span data-offset-key="dd4d1bf33bdb4079b70486c8adbc68b4:6"> to redirect the host to your localhost. However this edit requires admin access and it has the downside that it affects all other applications at the same time.</span>

</span>

</span>

<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="09dc6a1f42e34f8793d5459a4ec705c5">

<span data-offset-key="09dc6a1f42e34f8793d5459a4ec705c5:0">Change the Host: header</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="dffc8f0dfb0b4c62a66deaa6eee8ec70">

<span data-offset-key="dffc8f0dfb0b4c62a66deaa6eee8ec70:0">The </span>

<span data-offset-key="dffc8f0dfb0b4c62a66deaa6eee8ec70:1">`Host:`</span>

<span data-offset-key="dffc8f0dfb0b4c62a66deaa6eee8ec70:2"> header is the normal way an HTTP client tells the HTTP server which server it speaks to, as typically an HTTP server serves many different names using the same software instance.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="61f95271d2e8404783f2465950e1ff24">

<span data-offset-key="61f95271d2e8404783f2465950e1ff24:0">So, by passing in a custom modified </span>

<span data-offset-key="61f95271d2e8404783f2465950e1ff24:1">`Host:`</span>

<span data-offset-key="61f95271d2e8404783f2465950e1ff24:2"> header you can have the server respond with the contents of the site even when you did not actually connect to that host name.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="066084ed76e64a5abe2a4ff4434b3ca9">

<span data-offset-key="066084ed76e64a5abe2a4ff4434b3ca9:0">For example, you run a test instance of your main site </span>

<span data-offset-key="066084ed76e64a5abe2a4ff4434b3ca9:1">`www.example.com`</span>

<span data-offset-key="066084ed76e64a5abe2a4ff4434b3ca9:2"> on your local machine and you want to have curl ask for the index html:</span>

</span>

</span> curl -H "Host: www.example.com" http://localhost/<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="789ccb5b216e4eb680735b41b88bc413">

<span data-offset-key="789ccb5b216e4eb680735b41b88bc413:0">When setting a custom </span>

<span data-offset-key="789ccb5b216e4eb680735b41b88bc413:1">`Host:`</span>

<span data-offset-key="789ccb5b216e4eb680735b41b88bc413:2"> header and using cookies, curl will extract the custom name and use that as host when matching cookies to send off.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="19ce26a4be164ce0a9f127716b224030">

<span data-offset-key="19ce26a4be164ce0a9f127716b224030:0">The </span>

<span data-offset-key="19ce26a4be164ce0a9f127716b224030:1">`Host:`</span>

<span data-offset-key="19ce26a4be164ce0a9f127716b224030:2"> header is not enough when communicating with an HTTPS server. With HTTPS there's a separate extension field in the TLS protocol called SNI (Server Name Indication) that lets the client tell the server the name of the server it wants to talk to. curl will only extract the SNI name to send from the given URL.</span>

</span>

</span>

<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="8e8e26599e1f4252ba56df1d290d1fef">

<span data-offset-key="8e8e26599e1f4252ba56df1d290d1fef:0">Provide a custom IP address for a name</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c28ae775b12243c497171ee7477f100a">

<span data-offset-key="c28ae775b12243c497171ee7477f100a:0">Do you know better than the name resolver where curl should go? Then you can give an IP address to curl yourself! If you want to redirect port 80 access for </span>

<span data-offset-key="c28ae775b12243c497171ee7477f100a:1">`example.com`</span>

<span data-offset-key="c28ae775b12243c497171ee7477f100a:2"> to instead reach your localhost:</span>

</span>

</span> curl --resolve example.com:80:127.0.0.1 http://example.com/<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="cbef07cdd4c24be983a47406c5f8303f">

<span data-offset-key="cbef07cdd4c24be983a47406c5f8303f:0">You can even specify multiple </span>

<span data-offset-key="cbef07cdd4c24be983a47406c5f8303f:1">`--resolve`</span>

<span data-offset-key="cbef07cdd4c24be983a47406c5f8303f:2"> switches to provide multiple redirects of this sort, which can be handy if the URL you work with uses HTTP redirects or if you just want to have your command line work with multiple URLs.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="87c645b5714945faa6bac1e194f0933a">

<span data-offset-key="87c645b5714945faa6bac1e194f0933a:0">`--resolve`</span>

<span data-offset-key="87c645b5714945faa6bac1e194f0933a:1"> inserts the address into curl's DNS cache, so it will effectively make curl believe that's the address it got when it resolved the name.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="568d00f922db41ea8d7d065e68482449">

<span data-offset-key="568d00f922db41ea8d7d065e68482449:0">When talking HTTPS, this will send SNI for the name in the URL and curl will verify the server's response to make sure it serves for the name in the URL.</span>

</span>

</span>

<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="871cd2fdf23b4c0399419825f759a18e">

<span data-offset-key="871cd2fdf23b4c0399419825f759a18e:0">Provide a replacement name</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a11204b9e3bb4f1fa3d632919a95e64f">

<span data-offset-key="a11204b9e3bb4f1fa3d632919a95e64f:0">As a close relative to the </span>

<span data-offset-key="a11204b9e3bb4f1fa3d632919a95e64f:1">`--resolve`</span>

<span data-offset-key="a11204b9e3bb4f1fa3d632919a95e64f:2"> option, the </span>

<span data-offset-key="a11204b9e3bb4f1fa3d632919a95e64f:3">`--connect-to`</span>

<span data-offset-key="a11204b9e3bb4f1fa3d632919a95e64f:4"> option provides a minor variation. It allows you to specify a replacement name and port number for curl to use under the hood when a specific name and port number is used to connect.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="5861d0906f184eebbf4a012cc7ef736a">

<span data-offset-key="5861d0906f184eebbf4a012cc7ef736a:0">For example, suppose you have a single site called </span>

<span data-offset-key="5861d0906f184eebbf4a012cc7ef736a:1">`www.example.com`</span>

<span data-offset-key="5861d0906f184eebbf4a012cc7ef736a:2"> that in turn is actually served by three different individual HTTP servers: load1, load2 and load3, for load balancing purposes. In a typical normal procedure, curl resolves the main site and gets to speak to one of the load balanced servers (as it gets a list back and just picks one of them) and all is well. If you want to send a test request to one specific server out of the load balanced set (</span>

<span data-offset-key="5861d0906f184eebbf4a012cc7ef736a:3">`load1.example.com`</span>

<span data-offset-key="5861d0906f184eebbf4a012cc7ef736a:4"> for example) you can instruct curl to do that.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9ab7b066421d4a7e922028f8b6e63d90">

<span data-offset-key="9ab7b066421d4a7e922028f8b6e63d90:0">You </span>

<span data-offset-key="9ab7b066421d4a7e922028f8b6e63d90:1">_can_</span>

<span data-offset-key="9ab7b066421d4a7e922028f8b6e63d90:2"> still use </span>

<span data-offset-key="9ab7b066421d4a7e922028f8b6e63d90:3">`--resolve`</span>

<span data-offset-key="9ab7b066421d4a7e922028f8b6e63d90:4"> to accomplish this if you know the specific IP address of load1. But without having to first resolve and fix the IP address separately, you can tell curl:</span>

</span>

</span> curl --connect-to www.example.com:80:load1.example.com:80 http://www.example.com<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="1a2887ff5e4d4fd6b871ec2169b81194">

<span data-offset-key="1a2887ff5e4d4fd6b871ec2169b81194:0">It redirects from a SOURCE NAME + SOURCE PORT to a DESTINATION NAME + DESTINATION PORT. curl will then resolve the </span>

<span data-offset-key="1a2887ff5e4d4fd6b871ec2169b81194:1">`load1.example.com`</span>

<span data-offset-key="1a2887ff5e4d4fd6b871ec2169b81194:2"> name and connect, but in all other ways still assume it is talking to </span>

<span data-offset-key="1a2887ff5e4d4fd6b871ec2169b81194:3">`www.example.com`</span>

<span data-offset-key="1a2887ff5e4d4fd6b871ec2169b81194:4">.</span>

</span>

</span>

<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="5b7d587126414566832bc6945b7c129a">

<span data-offset-key="5b7d587126414566832bc6945b7c129a:0">Name resolve tricks with c-ares</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2b9186f22a9440d6bdbb7d54e4c6e281">

<span data-offset-key="2b9186f22a9440d6bdbb7d54e4c6e281:0">As should be detailed elsewhere in this book, curl may be built with several different name resolving backends. One of those backends is powered by the c-ares library and when curl is built to use c-ares, it gets a few extra superpowers that curl built to use other name resolve backends do not get. Namely, it gains the ability to more specifically instruct what DNS servers to use and how that DNS traffic is using the network.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7be4e42d5e6d4b1784f1b897b9090d9d">

<span data-offset-key="7be4e42d5e6d4b1784f1b897b9090d9d:0">With </span>

<span data-offset-key="7be4e42d5e6d4b1784f1b897b9090d9d:1">`--dns-servers`</span>

<span data-offset-key="7be4e42d5e6d4b1784f1b897b9090d9d:2">, you can specify exactly which DNS server curl should use instead of the default one. This lets you run your own experimental server that answers differently, or use a backup one if your regular one is unreliable or dead.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="74a6e87c942141f3a222e76506997bad">

<span data-offset-key="74a6e87c942141f3a222e76506997bad:0">With </span>

<span data-offset-key="74a6e87c942141f3a222e76506997bad:1">`--dns-ipv4-addr`</span>

<span data-offset-key="74a6e87c942141f3a222e76506997bad:2"> and </span>

<span data-offset-key="74a6e87c942141f3a222e76506997bad:3">`--dns-ipv6-addr`</span>

<span data-offset-key="74a6e87c942141f3a222e76506997bad:4"> you ask curl to "bind" its local end of the DNS communication to a specific IP address and with </span>

<span data-offset-key="74a6e87c942141f3a222e76506997bad:5">`--dns-interface`</span>

<span data-offset-key="74a6e87c942141f3a222e76506997bad:6"> you can instruct curl to use a specific network interface to use for its DNS requests.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="13ccba3489714ac7b6bb11b3956fe192">

<span data-offset-key="13ccba3489714ac7b6bb11b3956fe192:0">These </span>

<span data-offset-key="13ccba3489714ac7b6bb11b3956fe192:1">`--dns-*`</span>

<span data-offset-key="13ccba3489714ac7b6bb11b3956fe192:2"> options are advanced and are only meant for people who know what they are doing and understand what these options do. But they offer customizable DNS name resolution operations.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="93f093f59595464db29d14b820348057">

<span data-offset-key="93f093f59595464db29d14b820348057:0">Connection timeout</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8fd46c9754754d40a670277b2e7d7979">

<span data-offset-key="8fd46c9754754d40a670277b2e7d7979:0">curl will typically make a TCP connection to the host as an initial part of its network transfer. This TCP connection can fail or be slow, if there are shaky network conditions or faulty remote servers.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f75ded77c1c2490b9d6669fae51d384c">

<span data-offset-key="f75ded77c1c2490b9d6669fae51d384c:0">To reduce the impact on your scripts or other use, you can set the maximum time in seconds which curl will allow for the connection attempt. With </span>

<span data-offset-key="f75ded77c1c2490b9d6669fae51d384c:1">`--connect-timeout`</span>

<span data-offset-key="f75ded77c1c2490b9d6669fae51d384c:2"> you tell curl the maximum time to allow for connecting, and if curl has not connected in that time it returns a failure.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="111f169f93284bbcbe85c46415801331">

<span data-offset-key="111f169f93284bbcbe85c46415801331:0">The connection timeout only limits the time curl is allowed to spend up until the moment it connects, so once the TCP connection has been established it can take longer time. See the </span>

</span>

<a href="timeouts.html" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="0b9a296722cf439ba9bde2e0e95cd526">

<span data-offset-key="0b9a296722cf439ba9bde2e0e95cd526:0">Timeouts</span>

</span>

</a>

<span data-key="6b1eb578c25e40cba994c5cfcfb1d4ae">

<span data-offset-key="6b1eb578c25e40cba994c5cfcfb1d4ae:0"> section for more on generic curl timeouts.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9f2bed867bfb456f978d170a731387a7">

<span data-offset-key="9f2bed867bfb456f978d170a731387a7:0">If you specify a low timeout, you effectively disable curl's ability to connect to remote servers, slow servers or servers you access over unreliable networks.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0058bbf0c8db42a09f0fd174e59b48f2">

<span data-offset-key="0058bbf0c8db42a09f0fd174e59b48f2:0">The connection timeout can be specified as a decimal value for sub-second precision. For example, to allow 2781 milliseconds to connect:</span>

</span>

</span> curl --connect-timeout 2.781 https://example.com/<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="110c9a77b187476b88ef06adcba53f1a">

<span data-offset-key="110c9a77b187476b88ef06adcba53f1a:0">Network interface</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="82e15fac8fb44ab38682465d4c0ab9cb">

<span data-offset-key="82e15fac8fb44ab38682465d4c0ab9cb:0">On machines with multiple network interfaces that are connected to multiple networks, there are situations where you can decide which network interface you would prefer the outgoing network traffic to use. Or which originating IP address (out of the multiple ones you have) to use in the communication.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0bf5028b34a84dac8a48cee83a78d6be">

<span data-offset-key="0bf5028b34a84dac8a48cee83a78d6be:0">Tell curl which network interface, which IP address or even host name that you would like to "bind" your local end of the communication to, with the </span>

<span data-offset-key="0bf5028b34a84dac8a48cee83a78d6be:1">`--interface`</span>

<span data-offset-key="0bf5028b34a84dac8a48cee83a78d6be:2"> option:</span>

</span>

</span> curl --interface eth1 https://www.example.com/​curl --interface 192.168.0.2 https://www.example.com/​curl --interface machine2 https://www.example.com/<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="a232012fca754fc69911c6f6b7374eb0">

<span data-offset-key="a232012fca754fc69911c6f6b7374eb0:0">Local port number</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a010c5efd2114ebc8208630f120259bf">

<span data-offset-key="a010c5efd2114ebc8208630f120259bf:0">A TCP connection is created between an IP address and a port number in the local end and an IP address and a port number in the remote end. The remote port number can be specified in the URL and usually helps identify which service you are targeting.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c468caa82daa44159d73adfb1657058b">

<span data-offset-key="c468caa82daa44159d73adfb1657058b:0">The local port number is usually randomly assigned to your TCP connection by the network stack and you normally do not have to think about it much further. However, in some circumstances you find yourself behind network equipment, firewalls or similar setups that put restrictions on what source port numbers that can be allowed to set up the outgoing connections.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0e4afed1a9a74d2fb1ae3a76d0f3f9a9">

<span data-offset-key="0e4afed1a9a74d2fb1ae3a76d0f3f9a9:0">For situations like this, you can specify which local ports curl should bind the connection to. You can specify a single port number to use, or a range of ports. We recommend using a range because ports are scarce resources and the exact one you want may already be in use. If you ask for a local port number (or range) that curl cannot obtain for you, it will exit with a failure.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="aa66d43816274e34b0db73837f20446f">

<span data-offset-key="aa66d43816274e34b0db73837f20446f:0">Also, on most operating systems you cannot bind to port numbers below 1024 without having a higher privilege level (root) and we generally advise against running curl as root if you can avoid it.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="833062ffb4f748f885578b90001866f0">

<span data-offset-key="833062ffb4f748f885578b90001866f0:0">Ask curl to use a local port number between 4000 and 4200 when getting this HTTPS page:</span>

</span>

</span> curl --local-port 4000-4200 https://example.com/<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="ee4ec74c61b847668ee76a8ff161b203">

<span data-offset-key="ee4ec74c61b847668ee76a8ff161b203:0">Keep alive</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="021cdd9f027f4656840dd62527501a6f">

<span data-offset-key="021cdd9f027f4656840dd62527501a6f:0">TCP connections can be totally without traffic in either direction when they are not used. A totally idle connection can therefore not be clearly separated from a connection that has gone completely stale because of network or server issues.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e8c7ef5667534d8d911710cbd5ebebdd">

<span data-offset-key="e8c7ef5667534d8d911710cbd5ebebdd:0">At the same time, lots of network equipment such as firewalls or NATs are keeping track of TCP connections these days, so that they can translate addresses, block "wrong" incoming packets, etc. These devices often count completely idle connections as dead after N minutes, where N varies between device to device but at times is as short as 10 minutes or even less.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="36ba355f6a7545b3887692115569504c">

<span data-offset-key="36ba355f6a7545b3887692115569504c:0">One way to help avoid a really slow connection (or an idle one) getting treated as dead and wrongly killed, is to make sure TCP keep alive is used. TCP keepalive is a feature in the TCP protocol that makes it send "ping frames" back and forth when it would otherwise be totally idle. It helps idle connections to detect breakage even when no traffic is moving over it, and helps intermediate systems not consider the connection dead.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="dd5f195feac7424782569939b0b5579e">

<span data-offset-key="dd5f195feac7424782569939b0b5579e:0">curl uses TCP keepalive by default for the reasons mentioned here. But there might be times when you want to </span>

<span data-offset-key="dd5f195feac7424782569939b0b5579e:1">_disable_</span>

<span data-offset-key="dd5f195feac7424782569939b0b5579e:2"> keepalive or you may want to change the interval between the TCP "pings" (curl defaults to 60 seconds). You can switch off keepalive with:</span>

</span>

</span> curl --no-keepalive https://example.com/<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="99346600a24247b8951e6519a9a924a8">

<span data-offset-key="99346600a24247b8951e6519a9a924a8:0">or change the interval to 5 minutes (300 seconds) with:</span>

</span>

</span> curl --keepalive-time 300 https://example.com/<a href="uploads.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Uploads</span>

<a href="timeouts.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Timeouts</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="connections.html#name-resolve-tricks" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Name resolve tricks</span>

</span>

<a href="connections.html#edit-the-hosts-file" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Edit the hosts file</span>

</span>

<a href="connections.html#change-the-host-header" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Change the Host: header</span>

</span>

<a href="connections.html#provide-a-custom-ip-address-for-a-name" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Provide a custom IP address for a name</span>

</span>

<a href="connections.html#provide-a-replacement-name" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Provide a replacement name</span>

</span>

<a href="connections.html#name-resolve-tricks-with-c-ares" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Name resolve tricks with c-ares</span>

</span>

<a href="connections.html#connection-timeout" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Connection timeout</span>

</span>

<a href="connections.html#network-interface" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Network interface</span>

</span>

<a href="connections.html#local-port-number" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Local port number</span>

</span>

<a href="connections.html#keep-alive" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Keep alive</span>

</span>
