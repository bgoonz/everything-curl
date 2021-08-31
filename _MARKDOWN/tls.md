
<a href="telnet.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
</a>
<a href="tls/sslkeylogfile.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">SSLKEYLOGFILE</span>
</a># <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">TLS</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="5e43ce97c2884bf3a8dae08a6d41af6d">
<span data-offset-key="5e43ce97c2884bf3a8dae08a6d41af6d:0">TLS stands for Transport Layer Security and is the name for the technology that was formerly called SSL. The term SSL has not really died though so these days both the terms TLS and SSL are often used interchangeably to describe the same thing.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="188c33105dbf4dde8c29176f808195ff">
<span data-offset-key="188c33105dbf4dde8c29176f808195ff:0">TLS is a cryptographic security layer "on top" of TCP that makes the data tamper proof and guarantees server authenticity, based on strong public key cryptography and digital signatures.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="74260da46c7b4005a088777cc5666b16">
<span data-offset-key="74260da46c7b4005a088777cc5666b16:0">Ciphers</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="efcf7276e9e14abcb99b2de677f614f4">
<span data-offset-key="efcf7276e9e14abcb99b2de677f614f4:0">When curl connects to a TLS server, it negotiates how to speak the protocol and that negotiation involves several parameters and variables that both parties need to agree to. One of the parameters is which cryptography algorithms to use, the so called cipher. Over time, security researchers figure out flaws and weaknesses in existing ciphers and they are gradually phased out over time.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="3c1a4e5ea006463ea8a978313e6c3ada">
<span data-offset-key="3c1a4e5ea006463ea8a978313e6c3ada:0">Using the verbose option, </span>
<span data-offset-key="3c1a4e5ea006463ea8a978313e6c3ada:1">`-v`</span>
<span data-offset-key="3c1a4e5ea006463ea8a978313e6c3ada:2">, you can get information about which cipher and TLS version are negotiated. By using the </span>
<span data-offset-key="3c1a4e5ea006463ea8a978313e6c3ada:3">`--ciphers`</span>
<span data-offset-key="3c1a4e5ea006463ea8a978313e6c3ada:4"> option, you can change what cipher to prefer in the negotiation, but mind you, this is a power feature that takes knowledge to know how to use in ways that do not just make things worse.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="426fac17080643458ae71c31825b3ed8">
<span data-offset-key="426fac17080643458ae71c31825b3ed8:0">Enable TLS</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="21f8e87db84243faa73b670a3d520d4b">
<span data-offset-key="21f8e87db84243faa73b670a3d520d4b:0">curl supports the TLS version of many protocols. HTTP has HTTPS, FTP has FTPS, LDAP has LDAPS, POP3 has POP3S, IMAP has IMAPS and SMTP has SMTPS.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="8136cca7d4a94acb8df2c48b9d769a1f">
<span data-offset-key="8136cca7d4a94acb8df2c48b9d769a1f:0">If the server side supports it, you can use the TLS version of these protocols with curl.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="28be41a135b149a5b6823b1de92fecde">
<span data-offset-key="28be41a135b149a5b6823b1de92fecde:0">There are two general approaches to do TLS with protocols. One of them is to speak TLS already from the first connection handshake while the other is to "upgrade" the connection from plain-text to TLS using protocol specific instructions.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="e3d5c579ca0a4c28809ff10456f2ee2d">
<span data-offset-key="e3d5c579ca0a4c28809ff10456f2ee2d:0">With curl, if you explicitly specify the TLS version of the protocol (the one that has a name that ends with an 'S' character) in the URL, curl will try to connect with TLS from start, while if you specify the non-TLS version in the URL you can </span>
<span data-offset-key="e3d5c579ca0a4c28809ff10456f2ee2d:1">_usually_</span>
<span data-offset-key="e3d5c579ca0a4c28809ff10456f2ee2d:2"> upgrade the connection to TLS-based with the </span>
<span data-offset-key="e3d5c579ca0a4c28809ff10456f2ee2d:3">`--ssl`</span>
<span data-offset-key="e3d5c579ca0a4c28809ff10456f2ee2d:4"> option.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="49f0ccd468494009b20da4a53486a4b3">
<span data-offset-key="49f0ccd468494009b20da4a53486a4b3:0">The support table looks like this:</span>
</span>
</span>
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td style="text-align: left;">
<p>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">
<span data-key="0955a6d54b894943b4bee7abf9686d1d">
<span data-offset-key="0955a6d54b894943b4bee7abf9686d1d:0">Clear</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">
<span data-key="cb66fdc6765948ff9b38be040c00766b">
<span data-offset-key="cb66fdc6765948ff9b38be040c00766b:0">TLS version</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">
<span data-key="1a3e890ecd4941df850ff22af7a95e5b">
<span data-offset-key="1a3e890ecd4941df850ff22af7a95e5b:0">--ssl</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="even">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="d14e98f5d8854a9cae97390ad66b636d">
<span data-offset-key="d14e98f5d8854a9cae97390ad66b636d:0">HTTP</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="b3e813334d0842938e8913585d1d9362">
<span data-offset-key="b3e813334d0842938e8913585d1d9362:0">HTTPS</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="40ae2664c1d442719d3d7d3a2ce6aac4">
<span data-offset-key="40ae2664c1d442719d3d7d3a2ce6aac4:0">no</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="odd">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="25125212d2754d01b3fa24922599e936">
<span data-offset-key="25125212d2754d01b3fa24922599e936:0">LDAP</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="e71eeea297864895b01e6b859df7ac53">
<span data-offset-key="e71eeea297864895b01e6b859df7ac53:0">LDAPS</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="47b57d51d39c4d2cb428b4a0ace55df5">
<span data-offset-key="47b57d51d39c4d2cb428b4a0ace55df5:0">no</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="even">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="8a7cd157c68f4002960abd9ce1bb2271">
<span data-offset-key="8a7cd157c68f4002960abd9ce1bb2271:0">FTP</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="c1b58984c7a94ca795396efd9024e0e3">
<span data-offset-key="c1b58984c7a94ca795396efd9024e0e3:0">FTPS</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="60ddb58a17cd48edbf2ca4db94060be4">
<span data-offset-key="60ddb58a17cd48edbf2ca4db94060be4:0">
<strong>yes</strong>
</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="odd">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="8a49398b4174471db5808cdeb1b5d528">
<span data-offset-key="8a49398b4174471db5808cdeb1b5d528:0">POP3</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="95f79d35599a46a0b6db63c851125a27">
<span data-offset-key="95f79d35599a46a0b6db63c851125a27:0">POP3S</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="1f29c382a66c444582115839d0665880">
<span data-offset-key="1f29c382a66c444582115839d0665880:0">
<strong>yes</strong>
</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="even">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="e210e3c853fb4cbf8446c7daddb2d9ab">
<span data-offset-key="e210e3c853fb4cbf8446c7daddb2d9ab:0">IMAP</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="565dc3a8afd649ff813c793cde12c905">
<span data-offset-key="565dc3a8afd649ff813c793cde12c905:0">IMAPS</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="38758b90a22a40f6b73df62b8a646398">
<span data-offset-key="38758b90a22a40f6b73df62b8a646398:0">
<strong>yes</strong>
</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="odd">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="e21d7f16d84944eb9517d4e3dfcb35a3">
<span data-offset-key="e21d7f16d84944eb9517d4e3dfcb35a3:0">SMTP</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="04d7d85c95e2455d9638de6b41a5d1bc">
<span data-offset-key="04d7d85c95e2455d9638de6b41a5d1bc:0">SMTPS</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="e5afecf329e24b4e8b4bbb16b7cfda1a">
<span data-offset-key="e5afecf329e24b4e8b4bbb16b7cfda1a:0">
<strong>yes</strong>
</span>
</span>
</span>
</p>
</td>
</tr>
</tbody>
</table>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="43c05ccb84504fc791b0c8b3dadc92c6">
<span data-offset-key="43c05ccb84504fc791b0c8b3dadc92c6:0">The protocols that </span>
<span data-offset-key="43c05ccb84504fc791b0c8b3dadc92c6:1">_can_</span>
<span data-offset-key="43c05ccb84504fc791b0c8b3dadc92c6:2"> do </span>
<span data-offset-key="43c05ccb84504fc791b0c8b3dadc92c6:3">`--ssl`</span>
<span data-offset-key="43c05ccb84504fc791b0c8b3dadc92c6:4"> all favor that method. Using </span>
<span data-offset-key="43c05ccb84504fc791b0c8b3dadc92c6:5">`--ssl`</span>
<span data-offset-key="43c05ccb84504fc791b0c8b3dadc92c6:6"> means that curl will </span>
<span data-offset-key="43c05ccb84504fc791b0c8b3dadc92c6:7">_attempt_</span>
<span data-offset-key="43c05ccb84504fc791b0c8b3dadc92c6:8"> to upgrade the connection to TLS but if that fails, it will still continue with the transfer using the plain-text version of the protocol. To make the </span>
<span data-offset-key="43c05ccb84504fc791b0c8b3dadc92c6:9">`--ssl`</span>
<span data-offset-key="43c05ccb84504fc791b0c8b3dadc92c6:10"> option </span>
<span data-offset-key="43c05ccb84504fc791b0c8b3dadc92c6:11">**require**</span>
<span data-offset-key="43c05ccb84504fc791b0c8b3dadc92c6:12"> TLS to continue, there's instead the </span>
<span data-offset-key="43c05ccb84504fc791b0c8b3dadc92c6:13">`--ssl-reqd`</span>
<span data-offset-key="43c05ccb84504fc791b0c8b3dadc92c6:14"> option which will make the transfer fail if curl cannot successfully negotiate TLS.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="bfd04891287c4c06ae6c6f2c04072eb9">
<span data-offset-key="bfd04891287c4c06ae6c6f2c04072eb9:0">Require TLS security for your FTP transfer:</span>
</span>
</span>    curl --ssl-reqd ftp://ftp.example.com/file.txt<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="4ccc331530924ea0b684f64c4cf376ed">
<span data-offset-key="4ccc331530924ea0b684f64c4cf376ed:0">Suggest TLS to be used for your FTP transfer:</span>
</span>
</span>    curl --ssl ftp://ftp.example.com/file.txt<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="fed04906d2d3442a942cfc0069f9b3e0">
<span data-offset-key="fed04906d2d3442a942cfc0069f9b3e0:0">Connecting directly with TLS (to HTTPS://, LDAPS://, FTPS:// etc) means that TLS is mandatory and curl will return an error if TLS is not negotiated.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="3f6d3a06a8a24a659860c258a55c9b29">
<span data-offset-key="3f6d3a06a8a24a659860c258a55c9b29:0">Get a file over HTTPS:</span>
</span>
</span>    curl https://www.example.com/<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="cdefa3190508480a87353c9553aa2a65">
<span data-offset-key="cdefa3190508480a87353c9553aa2a65:0">SSL and TLS versions</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="6da5973b582845b28a5743fb44296626">
<span data-offset-key="6da5973b582845b28a5743fb44296626:0">SSL was invented in the mid 90s and has developed ever since. SSL version 2 was the first widespread version used on the Internet but that was deemed insecure already a long time ago. SSL version 3 took over from there, and it too has been deemed not safe enough for use.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="d208564df33c443aaf5ae8fe1df2b932">
<span data-offset-key="d208564df33c443aaf5ae8fe1df2b932:0">TLS version 1.0 was the first "standard". RFC 2246 was published 1999. TLS 1.1 came out in 2006, further improving security, followed by TLS 1.2 in 2008. TLS 1.2 came to be the gold standard for TLS for a decade.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="50a51d9bf66e4c95aa7bab72f5825f27">
<span data-offset-key="50a51d9bf66e4c95aa7bab72f5825f27:0">TLS 1.3 (RFC 8446) was finalized and published as a standard by the IETF in August 2018. This is the most secure and fastest TLS version as of date. It is however so new that a lot of software, tools and libraries do not yet support it.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="3918311f445d4ed28fd335e67269786b">
<span data-offset-key="3918311f445d4ed28fd335e67269786b:0">curl is designed to use a "safe version" of SSL/TLS by default. It means that it will not negotiate SSLv2 or SSLv3 unless specifically told to, and in fact several TLS libraries no longer provide support for those protocols so in many cases curl is not even able to speak those protocol versions unless you make a serious effort.</span>
</span>
</span>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td style="text-align: left;">
<p>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">
<span data-key="bc207651e4ed453b9d4dc14cd4f4acd4">
<span data-offset-key="bc207651e4ed453b9d4dc14cd4f4acd4:0">Option</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">
<span data-key="418b54cba4dd45cb83e730f0cd78a882">
<span data-offset-key="418b54cba4dd45cb83e730f0cd78a882:0">Use</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="even">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="a133c0b7d2094d279a2d1cbfa18939f2">
<span data-offset-key="a133c0b7d2094d279a2d1cbfa18939f2:0">--sslv2</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="87b698ac227f4b48b1f54f9bd9beda9f">
<span data-offset-key="87b698ac227f4b48b1f54f9bd9beda9f:0">SSL version 2</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="odd">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="b1188da77075466ab72d759c4a9d7bf0">
<span data-offset-key="b1188da77075466ab72d759c4a9d7bf0:0">--sslv3</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="f51f42e34e994fd9ba74bc0b3c4bb27d">
<span data-offset-key="f51f42e34e994fd9ba74bc0b3c4bb27d:0">SSL version 3</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="even">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="4ce57da5380948dd952c76cb8bec1cfb">
<span data-offset-key="4ce57da5380948dd952c76cb8bec1cfb:0">--tlsv1</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="ad9ee9045a43407dbb2022ff47054a01">
<span data-offset-key="ad9ee9045a43407dbb2022ff47054a01:0">TLS &gt;= version 1.0</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="odd">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="4176110ac0d642f0a1372b8c4677448d">
<span data-offset-key="4176110ac0d642f0a1372b8c4677448d:0">--tlsv1.0</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="e0a2ffffc8b74cb1b6ac356a11c8dff8">
<span data-offset-key="e0a2ffffc8b74cb1b6ac356a11c8dff8:0">TLS &gt;= version 1.0</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="even">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="d94b892c5d3943d995511a5ce33d536a">
<span data-offset-key="d94b892c5d3943d995511a5ce33d536a:0">--tlsv1.1</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="90d1a0c31b20454da998640ec48cc767">
<span data-offset-key="90d1a0c31b20454da998640ec48cc767:0">TLS &gt;= version 1.1</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="odd">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="42c7c95f82484ae48601312f39bb492d">
<span data-offset-key="42c7c95f82484ae48601312f39bb492d:0">--tlsv1.2</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="83cece0756cf466e96325a6b811b3364">
<span data-offset-key="83cece0756cf466e96325a6b811b3364:0">TLS &gt;= version 1.2</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="even">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="e39235466a7f42ddad0fd89bd133e1df">
<span data-offset-key="e39235466a7f42ddad0fd89bd133e1df:0">--tlsv1.3</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="9d3f220652354792b4d6b2fd22baca7c">
<span data-offset-key="9d3f220652354792b4d6b2fd22baca7c:0">TLS &gt;= version 1.3</span>
</span>
</span>
</p>
</td>
</tr>
</tbody>
</table>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="da47927eac6c4fa2a44420ce25e6fc08">
<span data-offset-key="da47927eac6c4fa2a44420ce25e6fc08:0">Verifying server certificates</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="462afcda87b5421287d1caaf016714a1">
<span data-offset-key="462afcda87b5421287d1caaf016714a1:0">Having a secure connection to a server is not worth a lot if you cannot also be certain that you are communicating with the </span>
<span data-offset-key="462afcda87b5421287d1caaf016714a1:1">**correct**</span>
<span data-offset-key="462afcda87b5421287d1caaf016714a1:2"> host. If we do not know that, we could just as well be talking with an impostor that just </span>
<span data-offset-key="462afcda87b5421287d1caaf016714a1:3">_appears_</span>
<span data-offset-key="462afcda87b5421287d1caaf016714a1:4"> to be who we think it is.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="5883e221cc044be69389815f6b9b81b5">
<span data-offset-key="5883e221cc044be69389815f6b9b81b5:0">To check that it communicates with the right TLS server, curl uses a set of locally stored CA certificates to verify the signature of the server's certificate. All servers provide a certificate to the client as part of the TLS handshake and all public TLS-using servers have acquired that certificate from an established Certificate Authority.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="97ae208e5f314a9ca4844140ce7af769">
<span data-offset-key="97ae208e5f314a9ca4844140ce7af769:0">After some applied crypto magic, curl knows that the server is in fact the correct one that acquired that certificate for the host name that curl used to connect to it. Failing to verify the server's certificate is a TLS handshake failure and curl exits with an error.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="fabe97f644e74e18831e4a3a264389f8">
<span data-offset-key="fabe97f644e74e18831e4a3a264389f8:0">In rare circumstances, you may decide that you still want to communicate with a TLS server even if the certificate verification fails. You then accept the fact that your communication may be subject to Man-In-The-Middle attacks. You lower your guards with the </span>
<span data-offset-key="fabe97f644e74e18831e4a3a264389f8:1">`-k`</span>
<span data-offset-key="fabe97f644e74e18831e4a3a264389f8:2"> or </span>
<span data-offset-key="fabe97f644e74e18831e4a3a264389f8:3">`--insecure`</span>
<span data-offset-key="fabe97f644e74e18831e4a3a264389f8:4"> option.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="5f1d3e34002f431787b66321ad8933b1">
<span data-offset-key="5f1d3e34002f431787b66321ad8933b1:0">CA store</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="822fe6b32dc645faa5abba44a8676372">
<span data-offset-key="822fe6b32dc645faa5abba44a8676372:0">curl needs a "CA store", a collection of CA certificates, to verify the TLS server it talks to.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="677eaec0cdf8467c8d6f4b1a17e372ab">
<span data-offset-key="677eaec0cdf8467c8d6f4b1a17e372ab:0">If curl is built to use a TLS library that is "native" to your platform, chances are that library will use the native CA store as well. If not, curl has to either have been built to know where the local CA store is, or users need to provide a path to the CA store when curl is invoked.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="e01f8ee4554f4016a286a61f849bfdcc">
<span data-offset-key="e01f8ee4554f4016a286a61f849bfdcc:0">You can point out a specific CA bundle to use in the TLS handshake with the </span>
<span data-offset-key="e01f8ee4554f4016a286a61f849bfdcc:1">`--cacert`</span>
<span data-offset-key="e01f8ee4554f4016a286a61f849bfdcc:2"> command line option. That bundle needs to be in PEM format. You can also set the environment variable </span>
<span data-offset-key="e01f8ee4554f4016a286a61f849bfdcc:3">`CURL_CA_BUNDLE`</span>
<span data-offset-key="e01f8ee4554f4016a286a61f849bfdcc:4"> to the full path.</span>
</span>
</span>
<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">
<span data-key="f21d50db79d440e6b2c56ef2f5e0984a">
<span data-offset-key="f21d50db79d440e6b2c56ef2f5e0984a:0">CA store on windows</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="fd6f7992ae4248dda79b26c50040c015">
<span data-offset-key="fd6f7992ae4248dda79b26c50040c015:0">curl built on windows that is not using the native TLS library (Schannel), have an extra sequence for how the CA store can be found and used.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="f1fe9d82dd494ed3a6b682e9e7ef3e41">
<span data-offset-key="f1fe9d82dd494ed3a6b682e9e7ef3e41:0">curl will search for a CA cert file named "curl-ca-bundle.crt" in these directories and in this order:</span>
</span>
</span>1.  <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="3518ad45d3b1419c94b79c4870f0e9fa">
<span data-offset-key="3518ad45d3b1419c94b79c4870f0e9fa:0">application's directory</span>
</span>
</span>2.  <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="9214aa4f22444ec3af7e9aa5512d9924">
<span data-offset-key="9214aa4f22444ec3af7e9aa5512d9924:0">current working directory</span>
</span>
</span>3.  <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="fa4b2066040b4aba8582b4544d8f8ed2">
<span data-offset-key="fa4b2066040b4aba8582b4544d8f8ed2:0">Windows System directory (e.g. </span>
<span data-offset-key="fa4b2066040b4aba8582b4544d8f8ed2:1">`C:\windows\system32`</span>
<span data-offset-key="fa4b2066040b4aba8582b4544d8f8ed2:2">)</span>
</span>
</span>4.  <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="141a3064b42e433d9486738e3475d7e8">
<span data-offset-key="141a3064b42e433d9486738e3475d7e8:0">Windows Directory (e.g. </span>
<span data-offset-key="141a3064b42e433d9486738e3475d7e8:1">`C:\windows`</span>
<span data-offset-key="141a3064b42e433d9486738e3475d7e8:2">)</span>
</span>
</span>5.  <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="aa63f92d44a745439e9c74715f5ecbf1">
<span data-offset-key="aa63f92d44a745439e9c74715f5ecbf1:0">all directories along </span>
<span data-offset-key="aa63f92d44a745439e9c74715f5ecbf1:1">`%PATH%`</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="fdb3f30c3e4e4860b213095b14be3d86">
<span data-offset-key="fdb3f30c3e4e4860b213095b14be3d86:0">Certificate pinning</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="fed88a8e084f43c69fd117c520512e00">
<span data-offset-key="fed88a8e084f43c69fd117c520512e00:0">TLS certificate pinning is a way to verify that the public key used to sign the servers certificate has not changed. It is "pinned".</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="3146644d549d4a3baf77359800a77adb">
<span data-offset-key="3146644d549d4a3baf77359800a77adb:0">When negotiating a TLS or SSL connection, the server sends a certificate indicating its identity. A public key is extracted from this certificate and if it does not exactly match the public key provided to this option, curl will abort the connection before sending or receiving any data.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="84fba339f11742a39bc2c0bcae61caff">
<span data-offset-key="84fba339f11742a39bc2c0bcae61caff:0">You tell curl a file name to read the sha256 value from, or you specify the base64 encoded hash directly in the command line with a </span>
<span data-offset-key="84fba339f11742a39bc2c0bcae61caff:1">`sha256//`</span>
<span data-offset-key="84fba339f11742a39bc2c0bcae61caff:2"> prefix. You can specify one or more hashes like that, separated with semicolons (;).</span>
</span>
</span>    curl --pinnedpubkey "sha256//83d34tasd3rt..." https://example.com/<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="e658f8c1aee84184a7383a990485fb82">
<span data-offset-key="e658f8c1aee84184a7383a990485fb82:0">This feature is not supported by all TLS backends.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="a4a69ad915b7427894be1072db3198a1">
<span data-offset-key="a4a69ad915b7427894be1072db3198a1:0">OCSP stapling</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="50961c9a76a84581ba2de074fdd7f3da">
<span data-offset-key="50961c9a76a84581ba2de074fdd7f3da:0">This uses the TLS extension called Certificate Status Request to ask the server to provide a fresh "proof" from the CA in the handshake, that the certificate that it returns is still valid. This is a way to make really sure the server's certificate has not been revoked.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="046dab3517634bee94b791dde2933b58">
<span data-offset-key="046dab3517634bee94b791dde2933b58:0">If the server does not support this extension, the test will fail and curl returns an error. And it is still far too common that servers do not support this.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="c984fde0d52e4e39a137c35161cf7012">
<span data-offset-key="c984fde0d52e4e39a137c35161cf7012:0">Ask for the handshake to use the status request like this:</span>
</span>
</span>    curl --cert-status https://example.com/<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="e64dcd52dbf14ad9a66b2e178b5ad320">
<span data-offset-key="e64dcd52dbf14ad9a66b2e178b5ad320:0">This feature is only supported by the OpenSSL, GnuTLS and NSS backends.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="a88c459dac504172af949c3fdc7add28">
<span data-offset-key="a88c459dac504172af949c3fdc7add28:0">Client certificates</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="2852bba20f4a40b88a63e7a3882e4ed1">
<span data-offset-key="2852bba20f4a40b88a63e7a3882e4ed1:0">TLS client certificates are a way for clients to cryptographically prove to servers that they are truly the right peer (also sometimes known as Mutual TLS or mTLS). A command line that uses a client certificate specifies the certificate and the corresponding key, and they are then passed on the TLS handshake with the server.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="a8b1f0c40c4e458e8d3b6a0c8bd5eecc">
<span data-offset-key="a8b1f0c40c4e458e8d3b6a0c8bd5eecc:0">You need to have your client certificate already stored in a file when doing this and you should supposedly have gotten it from the right instance via a different channel previously.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="c7854ba55c17468aa7022f46d9f40531">
<span data-offset-key="c7854ba55c17468aa7022f46d9f40531:0">The key is typically protected by a password that you need to provide or get prompted for interactively.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="37932f2d0353405b9589f05225aa7469">
<span data-offset-key="37932f2d0353405b9589f05225aa7469:0">curl offers options to let you specify a single file that is both the client certificate and the private key concatenated using </span>
<span data-offset-key="37932f2d0353405b9589f05225aa7469:1">`--cert`</span>
<span data-offset-key="37932f2d0353405b9589f05225aa7469:2">, or you can specify the key file independently with </span>
<span data-offset-key="37932f2d0353405b9589f05225aa7469:3">`--key`</span>
<span data-offset-key="37932f2d0353405b9589f05225aa7469:4">:</span>
</span>
</span>    curl --cert mycert:mypassword https://example.comcurl --cert mycert:mypassword --key mykey https://example.com<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="bc2de9ea31144847bedca5c540e92671">
<span data-offset-key="bc2de9ea31144847bedca5c540e92671:0">For some TLS backends you can also pass in the key and certificate using different types:</span>
</span>
</span>    curl --cert mycert:mypassword --cert-type PEM \     --key mykey --key-type PEM https://example.com<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="159910f06e8049c084096b3df64183e5">
<span data-offset-key="159910f06e8049c084096b3df64183e5:0">TLS auth</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="7a8f9ea23783445bbc36ee9b1ae8b5a8">
<span data-offset-key="7a8f9ea23783445bbc36ee9b1ae8b5a8:0">TLS connections offer a (rarely used) feature called Secure Remote Passwords. Using this, you authenticate the connection for the server using a name and password and the command line flags for this are </span>
<span data-offset-key="7a8f9ea23783445bbc36ee9b1ae8b5a8:1">`--tlsuser <name>`</span>
<span data-offset-key="7a8f9ea23783445bbc36ee9b1ae8b5a8:2"> and </span>
<span data-offset-key="7a8f9ea23783445bbc36ee9b1ae8b5a8:3">`--tlspassword <secret>`</span>
<span data-offset-key="7a8f9ea23783445bbc36ee9b1ae8b5a8:4">. Like this:</span>
</span>
</span>    curl --tlsuser daniel --tlspassword secret https://example.com<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="229b74626aea447780f2ac55adce03f0">
<span data-offset-key="229b74626aea447780f2ac55adce03f0:0">Different TLS backends</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="57785d2f56d44257802a9e7b663191d9">
<span data-offset-key="57785d2f56d44257802a9e7b663191d9:0">When curl is built, it gets told to use a specific TLS library. That TLS library is the engine that provides curl with the powers to speak TLS over the wire. We often refer to them as different "backends" as they can be seen as different plugglable pieces into the curl machine. curl can be built to be able to use one or more of these backends.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="3c01bad2855f4f2f8395527ad3e95379">
<span data-offset-key="3c01bad2855f4f2f8395527ad3e95379:0">Sometimes features and behaviors differ slightly when curl is built with different TLS backends, but the developers work hard on making those differences as small and unnoticable as possible.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="a88b65bdcac84809ba9ee1b4c1b6b8e3">
<span data-offset-key="a88b65bdcac84809ba9ee1b4c1b6b8e3:0">Showing the curl version information with </span>
</span>
<a href="https://github.com/bagder/everything-curl/tree/80575b1774f42028a706f684ebccb4b1efd19b31/usingcurl/usingcurl-version.md" class="link-a079aa82--primary-53a25e66--link-faf6c434">
<span data-key="b2232754dc20458d9390d0ebf784d18a">
<span data-offset-key="b2232754dc20458d9390d0ebf784d18a:0">curl --version</span>
</span>
</a>
<span data-key="3c889a46cbb84817bcc4f12cb1d73a0d">
<span data-offset-key="3c889a46cbb84817bcc4f12cb1d73a0d:0"> will always include the TLS library and version in the first line of output.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="fded010a2cfd496da185bf27e44cbf84">
<span data-offset-key="fded010a2cfd496da185bf27e44cbf84:0">Multiple TLS backends</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="904cb17f094a4876b16cc3ef0636af85">
<span data-offset-key="904cb17f094a4876b16cc3ef0636af85:0">When curl is built with </span>
<span data-offset-key="904cb17f094a4876b16cc3ef0636af85:1">_multiple_</span>
<span data-offset-key="904cb17f094a4876b16cc3ef0636af85:2"> TLS backends, it can be told which one to use each time it is started. It is always built to use a specific one by default unless one is asked for.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="45f7394f497449aabfaabea3d885e518">
<span data-offset-key="45f7394f497449aabfaabea3d885e518:0">If you invoke </span>
<span data-offset-key="45f7394f497449aabfaabea3d885e518:1">`curl --version`</span>
<span data-offset-key="45f7394f497449aabfaabea3d885e518:2"> for a curl with multiple backends it will mention </span>
<span data-offset-key="45f7394f497449aabfaabea3d885e518:3">`MultiSSL`</span>
<span data-offset-key="45f7394f497449aabfaabea3d885e518:4"> as a feature in the last line. The first line will then include all the supported TLS backends with the non-default ones within parentheses.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="baf1cc66ead14681a8cdce676ffc8acf">
<span data-offset-key="baf1cc66ead14681a8cdce676ffc8acf:0">To set a specific one to get used, set the environment variable </span>
<span data-offset-key="baf1cc66ead14681a8cdce676ffc8acf:1">`CURL_SSL_BACKEND`</span>
<span data-offset-key="baf1cc66ead14681a8cdce676ffc8acf:2"> to the name of it!</span>
</span>
</span>
<a href="telnet.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">
</a>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">TELNET</span>
<a href="tls/sslkeylogfile.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">
</a>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">SSLKEYLOGFILE</span>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 3 weeks ago</span>
<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>
<a href="tls.html#ciphers" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Ciphers</span>
</span>
<a href="tls.html#enable-tls" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Enable TLS</span>
</span>
<a href="tls.html#ssl-and-tls-versions" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">SSL and TLS versions</span>
</span>
<a href="tls.html#verifying-server-certificates" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Verifying server certificates</span>
</span>
<a href="tls.html#ca-store" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">CA store</span>
</span>
<a href="tls.html#ca-store-on-windows" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">CA store on windows</span>
</span>
<a href="tls.html#certificate-pinning" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Certificate pinning</span>
</span>
<a href="tls.html#ocsp-stapling" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">OCSP stapling</span>
</span>
<a href="tls.html#client-certificates" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Client certificates</span>
</span>
<a href="tls.html#tls-auth" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">TLS auth</span>
</span>
<a href="tls.html#different-tls-backends" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Different TLS backends</span>
</span>
<a href="tls.html#multiple-tls-backends" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Multiple TLS backends</span>
</span>
