<a href="version.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">
</a>
<a href="telnet.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
</a>
# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Version</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="eb8fde6266c34e4f915ac4ae14d59dd6">
<span data-offset-key="eb8fde6266c34e4f915ac4ae14d59dd6:0">Version</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="fc36d5d49508496a8a647ad82c19ba45">
<span data-offset-key="fc36d5d49508496a8a647ad82c19ba45:0">To get to know what version of curl you have installed, run</span>
</span>
</span>    curl --version<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="5845974d86784eed9c09b652fd91f2de">
<span data-offset-key="5845974d86784eed9c09b652fd91f2de:0">or use the shorthand version:</span>
</span>
</span>    curl -V<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="5d9fc31dada64ff7b8a8ea0098b4cafe">
<span data-offset-key="5d9fc31dada64ff7b8a8ea0098b4cafe:0">The output from that command line is typically four lines, out of which some will be rather long and might very well wrap in your terminal window.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="c85db840a85d49e2924b38b6a3de39e9">
<span data-offset-key="c85db840a85d49e2924b38b6a3de39e9:0">An example output from a Debian Linux as of June 2020:</span>
</span>
</span>    curl 7.68.0 (x86_64-pc-linux-gnu) libcurl/7.68.0 OpenSSL/1.1.1g zlib/1.2.11 brotli/1.0.7 libidn2/2.3.0 libpsl/0.21.0 (+libidn2/2.3.0) libssh2/1.8.0 nghttp2/1.41.0 librtmp/2.3Release-Date: 2020-01-08Protocols: dict file ftp ftps gopher http https imap imaps ldap ldaps pop3 pop3s rtmp rtsp scp sftp smb smbs smtp smtps telnet tftp Features: AsynchDNS brotli GSS-API HTTP2 HTTPS-proxy IDN IPv6 Kerberos Largefile libz NTLM NTLM_WB PSL SPNEGO SSL TLS-SRP UnixSockets<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="7747727638c243f49214b9d755d1d5ab">
<span data-offset-key="7747727638c243f49214b9d755d1d5ab:0">while the same command line invoked on a Windows 10 machine on the same date looks like:</span>
</span>
</span>    curl 7.55.1 (Windows) libcurl/7.55.1 WinSSLRelease-Date: [unreleased]Protocols: dict file ftp ftps http https imap imaps pop3 pop3s smtp smtps telnet tftpFeatures: AsynchDNS IPv6 Largefile SSPI Kerberos SPNEGO NTLM SSL<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="b2501b491def4ae5933c57686aecbefe">
<span data-offset-key="b2501b491def4ae5933c57686aecbefe:0">The meaning of the four lines?</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="29efc43313b04792af31dc3383f825f7">
<span data-offset-key="29efc43313b04792af31dc3383f825f7:0">Line 1: curl</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="4c3913d3205b404ba5faca02cb2deecd">
<span data-offset-key="4c3913d3205b404ba5faca02cb2deecd:0">The first line starts with </span>
<span data-offset-key="4c3913d3205b404ba5faca02cb2deecd:1">`curl`</span>
<span data-offset-key="4c3913d3205b404ba5faca02cb2deecd:2"> and first shows the main version number of the tool. Then follows the "platform" the tool was built for within parentheses and the libcurl version. Those three fields are common for all curl builds.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="56f48cebde3c470fa61aa0c1db2e7122">
<span data-offset-key="56f48cebde3c470fa61aa0c1db2e7122:0">If the curl version number has </span>
<span data-offset-key="56f48cebde3c470fa61aa0c1db2e7122:1">`-DEV`</span>
<span data-offset-key="56f48cebde3c470fa61aa0c1db2e7122:2"> appended to it, it means the version is built straight from a in-development source code and it is not an officially released and "blessed" version.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="5d6b33469a0e47708d6c3dfd2093a524">
<span data-offset-key="5d6b33469a0e47708d6c3dfd2093a524:0">The rest of this line contains names of third party components this build of curl uses, often with their invidual version number next to it with a slash separator. Like </span>
<span data-offset-key="5d6b33469a0e47708d6c3dfd2093a524:1">`OpenSSL/1.1.1g`</span>
<span data-offset-key="5d6b33469a0e47708d6c3dfd2093a524:2"> and </span>
<span data-offset-key="5d6b33469a0e47708d6c3dfd2093a524:3">`nghttp2/1.41.0`</span>
<span data-offset-key="5d6b33469a0e47708d6c3dfd2093a524:4">. This can for example tell you which TLS backends this curl uses.</span>
</span>
</span>
<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">
<span data-key="f9e2ff72d41a47249ffec295213281f3">
<span data-offset-key="f9e2ff72d41a47249ffec295213281f3:0">Line 1: TLS versions</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="48833a9827904ab48683e0fea79d09f8">
<span data-offset-key="48833a9827904ab48683e0fea79d09f8:0">Line 1 may contain one or more TLS libraries. curl can be built to support more than one TLS library which then makes curl - at startup - select which particular backend to use for this invoke.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="6bac1bd06feb47039cb36c20700b5f02">
<span data-offset-key="6bac1bd06feb47039cb36c20700b5f02:0">If curl supports more than one TLS library like this, the ones that are </span>
<span data-offset-key="6bac1bd06feb47039cb36c20700b5f02:1">_not_</span>
<span data-offset-key="6bac1bd06feb47039cb36c20700b5f02:2"> selected by default will be listed within parentheses. Thus, if you do not specify which backend to use use (with the </span>
<span data-offset-key="6bac1bd06feb47039cb36c20700b5f02:3">`CURL_SSL_BACKEND`</span>
<span data-offset-key="6bac1bd06feb47039cb36c20700b5f02:4"> environment variable) the one listed without parentheses will be used.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="2858940976ca4230941f97bec25a5012">
<span data-offset-key="2858940976ca4230941f97bec25a5012:0">Line 2: Release-Date</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="8d66c3a202904b53aa4b587044792dd2">
<span data-offset-key="8d66c3a202904b53aa4b587044792dd2:0">This line shows the date this curl version was released by the curl project, and it can also show a secondary "Patch date" if it has been updated somehow after it was originally released.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="fcb44825154d4ebe89978f497ea56c50">
<span data-offset-key="fcb44825154d4ebe89978f497ea56c50:0">This says </span>
<span data-offset-key="fcb44825154d4ebe89978f497ea56c50:1">`[unreleased]`</span>
<span data-offset-key="fcb44825154d4ebe89978f497ea56c50:2"> if curl was built another way than from a release tarball, and as you can see above that's how Microsft did it for Windows 10 and the curl project does not recommend it.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="f9db562225bc416581f744fcd2cec698">
<span data-offset-key="f9db562225bc416581f744fcd2cec698:0">Line 3: Protocols</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="be6f57bbae0a4d1aacf1244496227701">
<span data-offset-key="be6f57bbae0a4d1aacf1244496227701:0">This is a list of all transfer protocols (URL schemes really) in alphabetical order that this curl build supports. All names are shown in lowercase letters.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="cd8cc43e877c4315bf979d2553668716">
<span data-offset-key="cd8cc43e877c4315bf979d2553668716:0">As of curl 7.71.1 this list can contain these protocols:</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="3246aa6352ed4cb6b03632dfe1e4451a">
<span data-offset-key="3246aa6352ed4cb6b03632dfe1e4451a:0">dict, file, ftp, ftps, gopher, http, https, imap, imaps, ldap, ldaps, mqtt, pop3, pop3s, rtmp, rtsp, scp, sftp, smb, smbs, smtp, smtps, telnet and tftp</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="fefaf5fb0dc54869bfd5e5b8b75c3f2d">
<span data-offset-key="fefaf5fb0dc54869bfd5e5b8b75c3f2d:0">Line 4: Features</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="26e46dd72bb444218b5d581d83ab4e42">
<span data-offset-key="26e46dd72bb444218b5d581d83ab4e42:0">The list of features this build of curl supports. If the name is present in the list, that feature is enabled. If the name is not present, that feature is not enabled.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="da9b493b9a514e2ebc8b25439475b199">
<span data-offset-key="da9b493b9a514e2ebc8b25439475b199:0">Features that can be present there:</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="7a0d25f1f937423ba239bd0e125e3164">
<span data-offset-key="7a0d25f1f937423ba239bd0e125e3164:0">alt-svc - Support for the alt-svc: header</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="45668ecafcb744bba7a10781d2561baf">
<span data-offset-key="45668ecafcb744bba7a10781d2561baf:0">AsynchDNS - This curl uses asynchronous name resolves. Asynchronous name resolves can be done using either the c-ares or the threaded resolver backends.</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="b3191d429a0b4f06aeb7bde4203f7b98">
<span data-offset-key="b3191d429a0b4f06aeb7bde4203f7b98:0">brotli - support for automatic brotli compression over HTTP(S)</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="dc1348751f5f46de953b3128278630da">
<span data-offset-key="dc1348751f5f46de953b3128278630da:0">CharConv - curl was built with support for character set conversions (like EBCDIC)</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="3a63f0db49194096b8023683e4c1997c">
<span data-offset-key="3a63f0db49194096b8023683e4c1997c:0">Debug - This curl uses a libcurl built with Debug. This enables more error-tracking and memory debugging etc. For curl-developers only!</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="94134f45a66e4025a5cfc46658c8c67d">
<span data-offset-key="94134f45a66e4025a5cfc46658c8c67d:0">GSS-API - GSS-API authentication is enabled</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="7c77d1fc982c49de8b0aa56e30777365">
<span data-offset-key="7c77d1fc982c49de8b0aa56e30777365:0">HTTP2 - HTTP/2 support has been built-in.</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="b75ec4b19ad64592ba9a2e2905543c5a">
<span data-offset-key="b75ec4b19ad64592ba9a2e2905543c5a:0">HTTP3 - HTTP/3 support has been built-in.</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="61171e82011844699f77bdcbc7eeb9a6">
<span data-offset-key="61171e82011844699f77bdcbc7eeb9a6:0">HTTPS-proxy - This curl is built to support HTTPS proxy.</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="4aa9168294c24264856546266e80b4b9">
<span data-offset-key="4aa9168294c24264856546266e80b4b9:0">IDN - This curl supports IDN - international domain names.</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="e02aec07ae41406c9a3599873b7f357d">
<span data-offset-key="e02aec07ae41406c9a3599873b7f357d:0">IPv6 - You can use IPv6 with this.</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="5f27699a4eb348aa9cd28e062a0b1e75">
<span data-offset-key="5f27699a4eb348aa9cd28e062a0b1e75:0">krb4 - Krb4 for FTP is supported</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="ec49038374314a89ac4a89b77c7b5865">
<span data-offset-key="ec49038374314a89ac4a89b77c7b5865:0">Largefile - This curl supports transfers of large files, files larger than 2GB.</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="a260102731a644ecb61d49ff73f5cbbc">
<span data-offset-key="a260102731a644ecb61d49ff73f5cbbc:0">libz - Automatic gzip decompression of compressed files over HTTP is supported.</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="8e768762c42644ba84d094e78b4aed6f">
<span data-offset-key="8e768762c42644ba84d094e78b4aed6f:0">Metalink - This curl supports Metalink</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="e689ec4c22c14764b7732184bcb29b25">
<span data-offset-key="e689ec4c22c14764b7732184bcb29b25:0">MultiSSL - This curl supports multiple TLS backends.</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="cb69443fc30841979445421786711659">
<span data-offset-key="cb69443fc30841979445421786711659:0">NTLM - NTLM authentication is supported.</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="a72dd13e708a4c398c90b0456bf27272">
<span data-offset-key="a72dd13e708a4c398c90b0456bf27272:0">NTLM_WB - NTLM authentication is supported.</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="309c8568a0834f1eb3bacd20864b36a5">
<span data-offset-key="309c8568a0834f1eb3bacd20864b36a5:0">PSL - PSL is short for Public Suffix List and means that this curl has been built with knowledge about "public suffixes".</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="4d3a55e63d2d48eeb11112b0a84c822e">
<span data-offset-key="4d3a55e63d2d48eeb11112b0a84c822e:0">SPNEGO - SPNEGO authentication is supported.</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="602c8fc19f2a411a8015760eca01fc28">
<span data-offset-key="602c8fc19f2a411a8015760eca01fc28:0">SSL - SSL versions of various protocols are supported, such as HTTPS, FTPS, POP3S and so on.</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="cfb77b8dac4f4fafbdbdbab250a52b52">
<span data-offset-key="cfb77b8dac4f4fafbdbdbab250a52b52:0">SSPI - SSPI is supported</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="298f751987944961b2b29aa0d384e74a">
<span data-offset-key="298f751987944961b2b29aa0d384e74a:0">TLS-SRP - SRP (Secure Remote Password) authentication is supported for TLS.</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="50f5b8f1e8854385bdede593e11a8818">
<span data-offset-key="50f5b8f1e8854385bdede593e11a8818:0">UnixSockets - Unix sockets support is provided.</span>
</span>
</span>
<a href="verbose/writeout.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">
</a>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Write out</span>
<a href="persist.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">
</a>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Persistent connections</span>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 8 months ago</span>
<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>
<a href="version.html#version" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Version</span>
</span>
<a href="version.html#line-1-curl" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Line 1: curl</span>
</span>
<a href="version.html#line-1-tls-versions" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Line 1: TLS versions</span>
</span>
<a href="version.html#line-2-release-date" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Line 2: Release-Date</span>
</span>
<a href="version.html#line-3-protocols" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Line 3: Protocols</span>
</span>
<a href="version.html#line-4-features" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Line 4: Features</span>
</span>
