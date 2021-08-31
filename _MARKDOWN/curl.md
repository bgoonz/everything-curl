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

<a href="network.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Networking simplified</span></a>

<a href="protocols.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Protocols</span></a>

<a href="curl.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">curl protocols</span></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Command line basics</span>



<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">How to HTTP with curl</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">libcurl basics</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP with libcurl</span>

<a href="../bindings.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Bindings</span></a>

<a href="../internals.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">libcurl internals</span></a>

<a href="../bookindex.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f"></span></a>





# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">curl protocols</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2"></span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2"></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="7e4af117db1f4ab6a524f47c6899525b"><span data-offset-key="7e4af117db1f4ab6a524f47c6899525b:0">curl supports about 26 protocols. We say "about" because it depends on how you count and what you consider to be distinctly different protocols.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="809f0fa1a7aa4c8799bf06d2d5e22c5e"><span data-offset-key="809f0fa1a7aa4c8799bf06d2d5e22c5e:0">DICT</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="39a03b8637474a728354c3c15baf09e8"><span data-offset-key="39a03b8637474a728354c3c15baf09e8:0">DICT is a dictionary network protocol, it allows clients to ask dictionary servers about a meaning or explanation for words. See RFC 2229. Dict servers and clients use TCP port 2628.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="70fa921ac5eb4c0c8fd5c601835f59b6"><span data-offset-key="70fa921ac5eb4c0c8fd5c601835f59b6:0">FILE</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="fdf1ecbe3f0c466f90fd0071ac0305b7"><span data-offset-key="fdf1ecbe3f0c466f90fd0071ac0305b7:0">FILE is not actually a "network" protocol. It is a URL scheme that allows you to tell curl to get a file from the local file system instead of getting it over the network from a remote server. See RFC 1738.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="ebcf1c2e7087436da2ad72544d16432c"><span data-offset-key="ebcf1c2e7087436da2ad72544d16432c:0">FTP</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="7f1a74404ad44245a8fed72d452c0f2d"><span data-offset-key="7f1a74404ad44245a8fed72d452c0f2d:0">FTP stands for File Transfer Protocol and is an old (originates in the early 1970s) way to transfer files back and forth between a client and a server. See RFC 959. It has been extended greatly over the years. FTP servers and clients use TCP port 21 plus one more port, though the second one is usually dynamically established during communication.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="61ba2bce00e64971b7bcfe6e963496df"><span data-offset-key="61ba2bce00e64971b7bcfe6e963496df:0">See the external page </span></span><a href="https://daniel.haxx.se/docs/ftp-vs-http.html" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="340421fdb4724afc85043b1f94a7dc22"><span data-offset-key="340421fdb4724afc85043b1f94a7dc22:0">FTP vs HTTP</span></span></a><span data-key="d758640269354660b7e11db711124fae"><span data-offset-key="d758640269354660b7e11db711124fae:0"> for how it differs to HTTP.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="bdaeb0a081f14614abb15175d77fbbfb"><span data-offset-key="bdaeb0a081f14614abb15175d77fbbfb:0">FTPS</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="4661c8989251433a90360cbcf4bed6aa"><span data-offset-key="4661c8989251433a90360cbcf4bed6aa:0">FTPS stands for Secure File Transfer Protocol. It follows the tradition of appending an 'S' to the protocol name to signify that the protocol is done like normal FTP but with an added SSL/TLS security layer. See RFC 4217.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="e5cad4e1375942049a9f94a1a6eca737"><span data-offset-key="e5cad4e1375942049a9f94a1a6eca737:0">This protocol is problematic to use through firewalls and other network equipment.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="28c200cbd17a46e9a26fb01205acf50c"><span data-offset-key="28c200cbd17a46e9a26fb01205acf50c:0">GOPHER</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="4728ada018d943468715b5372c58fd9f"><span data-offset-key="4728ada018d943468715b5372c58fd9f:0">Designed for "distributing, searching, and retrieving documents over the Internet", Gopher is somewhat of the grand father to HTTP as HTTP has mostly taken over completely for the same use cases. See RFC 1436. Gopher servers and clients use TCP port 70.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="5b22c654e7894f30bc32f93a17fc93af"><span data-offset-key="5b22c654e7894f30bc32f93a17fc93af:0">GOPHERS</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="4bd09df8380a48f2a950faeede2367ad"><span data-offset-key="4bd09df8380a48f2a950faeede2367ad:0">Gopher over TLS. A recent extension to the very old protocol.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="2c4b0a96540945cfb6a31d800d36b239"><span data-offset-key="2c4b0a96540945cfb6a31d800d36b239:0">HTTP</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="78efb1c9ee2d4f169011d882fb737749"><span data-offset-key="78efb1c9ee2d4f169011d882fb737749:0">The Hypertext Transfer Protocol, HTTP, is the most widely used protocol for transferring data on the web and over the Internet. See RFC 7230 for HTTP/1.1 and RFC 7540 for </span></span><a href="https://github.com/bagder/everything-curl/tree/e0491fc8e31830524807d5ab5986525bebc217c8/protocols/http-http2.md" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="cdab3570adf34c9dbd2ae5a2063949d7"><span data-offset-key="cdab3570adf34c9dbd2ae5a2063949d7:0">HTTP/2</span></span></a><span data-key="16df40c25cc44393851a7c6ef8eadfd7"><span data-offset-key="16df40c25cc44393851a7c6ef8eadfd7:0">. HTTP servers and clients use TCP port 80.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="bca3d00ecbf4421eab8a70ea4774c94c"><span data-offset-key="bca3d00ecbf4421eab8a70ea4774c94c:0">HTTPS</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="89aa7e28c33f4e558de9b8bf306e5334"><span data-offset-key="89aa7e28c33f4e558de9b8bf306e5334:0">Secure HTTP is HTTP done over an SSL/TLS connection. See RFC 2818. HTTPS servers and clients use TCP port 443, unless they speak </span></span><a href="https://github.com/bagder/everything-curl/tree/e0491fc8e31830524807d5ab5986525bebc217c8/protocols/http-http3.md" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="39b608c4870746d292cc97129ea0f6e0"><span data-offset-key="39b608c4870746d292cc97129ea0f6e0:0">HTTP/3</span></span></a><span data-key="df86ffc1c05b42d6adce164ba3c8c994"><span data-offset-key="df86ffc1c05b42d6adce164ba3c8c994:0"> which then uses QUIC and is done over UDP...</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="d996092793c74596a0354492b9af212a"><span data-offset-key="d996092793c74596a0354492b9af212a:0">IMAP</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="3764545e74194dc88fd7381fd9626146"><span data-offset-key="3764545e74194dc88fd7381fd9626146:0">The Internet Message Access Protocol, IMAP, is a protocol for accessing, controlling and "reading" email. See RFC 3501. IMAP servers and clients use TCP port 143. Whilst connections to the server start out as cleartext, SSL/TLS communication may be supported by the client explicitly requesting to upgrade the connection using the </span><span data-offset-key="3764545e74194dc88fd7381fd9626146:1">`STARTTLS`</span><span data-offset-key="3764545e74194dc88fd7381fd9626146:2"> command. See RFC 2595.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="c149ba7924314850ba61dfbdecc2db62"><span data-offset-key="c149ba7924314850ba61dfbdecc2db62:0">IMAPS</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="9ae578c5fd1b4300a393219deac1dc2e"><span data-offset-key="9ae578c5fd1b4300a393219deac1dc2e:0">Secure IMAP is IMAP done over an SSL/TLS connection. Such connections implicitly start out using SSL/TLS and as such servers and clients use TCP port 993 to communicate with each other. See RFC 8314.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="e3004fe2379f4cec9cb0cd046ea7361b"><span data-offset-key="e3004fe2379f4cec9cb0cd046ea7361b:0">LDAP</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="195b40a6ab304bcd817b1822fa94363d"><span data-offset-key="195b40a6ab304bcd817b1822fa94363d:0">The Lightweight Directory Access Protocol, LDAP, is a protocol for accessing and maintaining distributed directory information. Basically a database lookup. See RFC 4511. LDAP servers and clients use TCP port 389.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="cc6b286d375e4a4cb1369b202d09178f"><span data-offset-key="cc6b286d375e4a4cb1369b202d09178f:0">LDAPS</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="f9821864eacd48eaa4c17dcc3b7592d1"><span data-offset-key="f9821864eacd48eaa4c17dcc3b7592d1:0">Secure LDAP is LDAP done over an SSL/TLS connection.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="c673e30d4575431cb0886c8999258916"><span data-offset-key="c673e30d4575431cb0886c8999258916:0">MQTT</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="495aed68b1f4484a8c5dd73d1d714abb"><span data-offset-key="495aed68b1f4484a8c5dd73d1d714abb:0">Message Queuing Telemetry Transport, MQTT, is a protocol commonly used in IoT systems for interchanging data mostly involving smaller devices. It is a so called "publish-subscribe" protocol.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="bc74913a8bbc454490060f749f647693"><span data-offset-key="bc74913a8bbc454490060f749f647693:0">POP3</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="b89be73b987f4e70b5f56b265779bad6"><span data-offset-key="b89be73b987f4e70b5f56b265779bad6:0">The Post Office Protocol version 3 (POP3) is a protocol for retrieving email from a server. See RFC 1939. POP3 servers and clients use TCP port 110. Whilst connections to the server start out as cleartext, SSL/TLS communication may be supported by the client explicitly requesting to upgrade the connection using the </span><span data-offset-key="b89be73b987f4e70b5f56b265779bad6:1">`STLS`</span><span data-offset-key="b89be73b987f4e70b5f56b265779bad6:2"> command. See RFC 2595.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="9ede0c2dc24d44699ce72f73a48002f4"><span data-offset-key="9ede0c2dc24d44699ce72f73a48002f4:0">POP3S</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="808dc7c30d77414b979972a0930c9eef"><span data-offset-key="808dc7c30d77414b979972a0930c9eef:0">Secure POP3 is POP3 done over an SSL/TLS connection. Such connections implicitly start out using SSL/TLS and as such servers and clients use TCP port 995 to communicate with each other. See RFC 8314.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="2221b2149edc496db5d386c919d76d11"><span data-offset-key="2221b2149edc496db5d386c919d76d11:0">RTMP</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="e3a52022f56d41f68cd31d79d1701624"><span data-offset-key="e3a52022f56d41f68cd31d79d1701624:0">The Real-Time Messaging Protocol (RTMP) is a protocol for streaming audio, video and data. RTMP servers and clients use TCP port 1935.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="d0b9f697d8f94512856bbb1fead6d5a9"><span data-offset-key="d0b9f697d8f94512856bbb1fead6d5a9:0">RTSP</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="986d98756e2b4a8897365a9544ed5308"><span data-offset-key="986d98756e2b4a8897365a9544ed5308:0">The Real Time Streaming Protocol (RTSP) is a network control protocol to control streaming media servers. See RFC 2326. RTSP servers and clients use TCP and UDP port 554.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="7799b2e36b4f470eba7d6f7ab750a7da"><span data-offset-key="7799b2e36b4f470eba7d6f7ab750a7da:0">SCP</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="8aef2c8058d74e3ca6cb29922973b537"><span data-offset-key="8aef2c8058d74e3ca6cb29922973b537:0">The Secure Copy (SCP) protocol is designed to copy files to and from a remote SSH server. SCP servers and clients use TCP port 22.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="5ce0f12c5aa24097be7b1335f54f32b2"><span data-offset-key="5ce0f12c5aa24097be7b1335f54f32b2:0">SFTP</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="115496cbc1cf4f80bb3ddd032ffabd06"><span data-offset-key="115496cbc1cf4f80bb3ddd032ffabd06:0">The SSH File Transfer Protocol (SFTP) that provides file access, file transfer, and file management over a reliable data stream. SFTP servers and clients use TCP port 22.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="c1541437e01b4f49a15fec8e890bca9f"><span data-offset-key="c1541437e01b4f49a15fec8e890bca9f:0">SMB</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="196d2f47a6534ec6bce2ece887f4cd26"><span data-offset-key="196d2f47a6534ec6bce2ece887f4cd26:0">The Server Message Block (SMB) protocol is also known as CIFS. It is an application-layer network protocol mainly used for providing shared access to files, printers, and serial ports and miscellaneous communications between nodes on a network. SMB servers and clients use TCP port 445.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="ec33f47bbdce43a3a2f0dcd2e12c39f3"><span data-offset-key="ec33f47bbdce43a3a2f0dcd2e12c39f3:0">SMBS</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="2f624c232746405084565b48c1da0fa3"><span data-offset-key="2f624c232746405084565b48c1da0fa3:0">SMB done over TLS.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="aed5a363e6ea4de888957df9d34eebc8"><span data-offset-key="aed5a363e6ea4de888957df9d34eebc8:0">SMTP</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="d244f887ff1049dd8d171d46d8f07fa5"><span data-offset-key="d244f887ff1049dd8d171d46d8f07fa5:0">The Simple Mail Transfer Protocol (SMTP) is a protocol for email transmission. See RFC 5321. SMTP servers and clients use TCP port 25. Whilst connections to the server start out as cleartext, SSL/TLS communication may be supported by the client explicitly requesting to upgrade the connection using the </span><span data-offset-key="d244f887ff1049dd8d171d46d8f07fa5:1">`STARTTLS`</span><span data-offset-key="d244f887ff1049dd8d171d46d8f07fa5:2"> command. See RFC 3207.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="853d1c4229cd47a39efa8fa65f693171"><span data-offset-key="853d1c4229cd47a39efa8fa65f693171:0">SMTPS</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="be9c9bd8ee27419aaba328bf365691ab"><span data-offset-key="be9c9bd8ee27419aaba328bf365691ab:0">Secure SMTP, sometimes called SSMTP, is SMTP done over an SSL/TLS connection. Such connections implicitly start out using SSL/TLS and as such servers and clients use TCP port 465 to communicate with each other. See RFC 8314.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="484f0a62f67b4b9dbe4175202105c74f"><span data-offset-key="484f0a62f67b4b9dbe4175202105c74f:0">TELNET</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="2d1636baa2704cfd9262e93dbf7871ab"><span data-offset-key="2d1636baa2704cfd9262e93dbf7871ab:0">TELNET is an application layer protocol used over networks to provide a bidirectional interactive text-oriented communication facility using a virtual terminal connection. See RFC 854. TELNET servers and clients use TCP port 23.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="5775ad24c1d84a098236d87bd5077f79"><span data-offset-key="5775ad24c1d84a098236d87bd5077f79:0">TFTP</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="5439ea9421a04e81a560811b407a36cd"><span data-offset-key="5439ea9421a04e81a560811b407a36cd:0">The Trivial File Transfer Protocol (TFTP) is a protocol for doing simple file transfers over UDP to get a file from or put a file onto a remote host. TFTP servers and clients use UDP port 69.</span></span></span>

<a href="protocols.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674"></a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Protocols</span>

<a href="../cmdline.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42"></a>


<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Command line basics</span>

<img src="https://avatars1.githubusercontent.com/u/965580?v=4" class="image-67b14f24--avatar-1c1d03ec" />



<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 months ago</span>



<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="curl.html#dict" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">DICT</span></span>

<a href="curl.html#file" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">FILE</span></span>

<a href="curl.html#ftp" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">FTP</span></span>

<a href="curl.html#ftps" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">FTPS</span></span>

<a href="curl.html#gopher" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">GOPHER</span></span>

<a href="curl.html#gophers" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">GOPHERS</span></span>

<a href="curl.html#http" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">HTTP</span></span>

<a href="curl.html#https" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">HTTPS</span></span>

<a href="curl.html#imap" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">IMAP</span></span>

<a href="curl.html#imaps" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">IMAPS</span></span>

<a href="curl.html#ldap" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">LDAP</span></span>

<a href="curl.html#ldaps" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">LDAPS</span></span>

<a href="curl.html#mqtt" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">MQTT</span></span>

<a href="curl.html#pop3" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">POP3</span></span>

<a href="curl.html#pop-3-s" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">POP3S</span></span>

<a href="curl.html#rtmp" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">RTMP</span></span>

<a href="curl.html#rtsp" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">RTSP</span></span>

<a href="curl.html#scp" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">SCP</span></span>

<a href="curl.html#sftp" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">SFTP</span></span>

<a href="curl.html#smb" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">SMB</span></span>

<a href="curl.html#smbs" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">SMBS</span></span>

<a href="curl.html#smtp" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">SMTP</span></span>

<a href="curl.html#smtps" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">SMTPS</span></span>

<a href="curl.html#telnet" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">TELNET</span></span>

<a href="curl.html#tftp" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">TFTP</span></span>
