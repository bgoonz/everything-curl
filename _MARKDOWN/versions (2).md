<a href="../index.html" class="link-a079aa82--primary-53a25e66--logoLink-10d08504"></a>

<img src="https://gblobscdn.gitbook.com/orgs%2F-LxuH0qSm4xO9nWfEBlB%2Favatar.png?alt=media" class="image-67b14f24--avatar-1c1d03ec" />

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1--spaceNameText-677c2969">Everything curl</span>

<a href="../index.html" class="link-a079aa82--primary-53a25e66--logoLink-10d08504"></a>

<img src="https://gblobscdn.gitbook.com/orgs%2F-LxuH0qSm4xO9nWfEBlB%2Favatar.png?alt=media" class="image-67b14f24--avatar-1c1d03ec" />

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1--spaceNameText-677c2969">Everything curl</span>

<a href="../index.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Introduction</span></a>

<a href="../how-to-read.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">How to read this book</span></a>





<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">How to HTTP with curl</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">libcurl basics</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP with libcurl</span>

<a href="responses.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP responses</span></a>

<a href="requests.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP requests</span></a>

<a href="versions.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP versions</span></a>

<a href="ranges.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP ranges</span></a>

<a href="auth.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP authentication</span></a>

<a href="cookies.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Cookies with libcurl</span></a>

<a href="download.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Download</span></a>

<a href="upload.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Upload</span></a>

<a href="../bindings.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Bindings</span></a>

<a href="../internals.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">libcurl internals</span></a>

<a href="../bookindex.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f"></span></a>





# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">HTTP versions</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2"></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="b531e58aac274e268200a4c7e6cc6708"><span data-offset-key="b531e58aac274e268200a4c7e6cc6708:0">As any other Internet protocol, the HTTP protocol has kept evolving over the years and now there are clients and servers distributed over the world and over time that speak different versions with varying levels of success. So in order to get libcurl to work with the URLs you pass in libcurl offers ways for you to specify which HTTP version that request and transfer should use. libcurl is designed in a way so that it tries to use the most common, the most sensible if you want, default values first but sometimes that is not enough and then you may need to instruct libcurl what to do.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="5b1d52b76f99453887da26c1ef8524be"><span data-offset-key="5b1d52b76f99453887da26c1ef8524be:0">Since mid 2016, libcurl defaults to use HTTP/2 for HTTPS servers if you have a libcurl that has HTTP/2 abilities built-in, libcurl will attempt to use HTTP/2 automatically or fall back to 1.1 in case the negotiation failed. Non-HTTP/2 capable libcurls get 1.1 over HTTPS by default. Plain HTTP requests still default to HTTP/1.1.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="7a669911caf84ee7b5ccac60c5fcf2d0"><span data-offset-key="7a669911caf84ee7b5ccac60c5fcf2d0:0">If the default behavior is not good enough for your transfer, the </span><span data-offset-key="7a669911caf84ee7b5ccac60c5fcf2d0:1">`CURLOPT_HTTP_VERSION`</span><span data-offset-key="7a669911caf84ee7b5ccac60c5fcf2d0:2"> option is there for you.</span></span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td style="text-align: left;"><p><span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1"><span data-key="ce2cbcc566cb4278b5ec60f79fab4219"><span data-offset-key="ce2cbcc566cb4278b5ec60f79fab4219:0">Option</span></span></span></p></td><td style="text-align: left;"><p><span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1"><span data-key="1d6d1a521b25488abe86eb272c9dafd9"><span data-offset-key="1d6d1a521b25488abe86eb272c9dafd9:0">Description</span></span></span></p></td></tr><tr class="even"><td style="text-align: left;"><p><span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="3782555de23c4b189b622e4ff2d5a286"><span data-offset-key="3782555de23c4b189b622e4ff2d5a286:0">CURL_HTTP_VERSION_NONE</span></span></span></p></td><td style="text-align: left;"><p><span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="47379cba41bc4947926813b7b80c0958"><span data-offset-key="47379cba41bc4947926813b7b80c0958:0">Reset back to default behavior</span></span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><p><span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="bc64056d8c92435eb3a89982b250aa84"><span data-offset-key="bc64056d8c92435eb3a89982b250aa84:0">CURL_HTTP_VERSION_1_0</span></span></span></p></td><td style="text-align: left;"><p><span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="80e1ee9c6b8245809e6c34be6b945eaa"><span data-offset-key="80e1ee9c6b8245809e6c34be6b945eaa:0">Enforce use of the legacy HTTP/1.0 protocol version</span></span></span></p></td></tr><tr class="even"><td style="text-align: left;"><p><span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="33f4cd1598e4450798fcfca8a9ad3c59"><span data-offset-key="33f4cd1598e4450798fcfca8a9ad3c59:0">CURL_HTTP_VERSION_1_1</span></span></span></p></td><td style="text-align: left;"><p><span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="7376270b628048929c93b8a45440bbb6"><span data-offset-key="7376270b628048929c93b8a45440bbb6:0">Do the request using the HTTP/1.1 protocol version</span></span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><p><span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="75edac1cdf4c4792b386521ca07317b1"><span data-offset-key="75edac1cdf4c4792b386521ca07317b1:0">CURL_HTTP_VERSION_2_0</span></span></span></p></td><td style="text-align: left;"><p><span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="7dba3774d4114aa3a5329c9e7e80d21a"><span data-offset-key="7dba3774d4114aa3a5329c9e7e80d21a:0">Attempt to use HTTP/2</span></span></span></p></td></tr><tr class="even"><td style="text-align: left;"><p><span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="77cd5be7c2064956a55f8bc15d130224"><span data-offset-key="77cd5be7c2064956a55f8bc15d130224:0">CURL_HTTP_VERSION_2TLS</span></span></span></p></td><td style="text-align: left;"><p><span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="655883a7964f46d78d1c2a9e245e28d0"><span data-offset-key="655883a7964f46d78d1c2a9e245e28d0:0">Attempt to use HTTP/2 on HTTPS connections only, otherwise do HTTP/1.1</span></span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><p><span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="b4046314a6184cf29c7696cc87ed37f3"><span data-offset-key="b4046314a6184cf29c7696cc87ed37f3:0">CURL_HTTP_VERSION_2_PRIOR_KNOWLEDGE</span></span></span></p></td><td style="text-align: left;"><p><span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="0470decb80b64681aadc7eff63898309"><span data-offset-key="0470decb80b64681aadc7eff63898309:0">Use HTTP/2 straight away without "upgrading" from 1.1. It requires that you know that this server is OK with it.</span></span></span></p></td></tr><tr class="even"><td style="text-align: left;"><p><span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="4e2dadacd43b4383934bf645e5816ef8"><span data-offset-key="4e2dadacd43b4383934bf645e5816ef8:0">CURL_HTTP_VERSION_3</span></span></span></p></td><td style="text-align: left;"><p><span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="c25007c055bf477385dadf9cc6911ca4"><span data-offset-key="c25007c055bf477385dadf9cc6911ca4:0">Use HTTP/3 straight away. It requires that you know that this server is OK with it.</span></span></span></p></td></tr></tbody></table>

<a href="requests.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674"></a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">HTTP requests</span>

<a href="ranges.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42"></a>


<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">HTTP ranges</span>



<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>


