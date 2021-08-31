h<a href="responses.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP responses</span>

</a>

<a href="requests.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP requests</span>

</a>

<a href="versions.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP versions</span>

</a>

<a href="ranges.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP ranges</span>

</a>

<a href="auth.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP authentication</span>

</a>

<a href="cookies.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Cookies with libcurl</span>

</a>

<a href="download.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Download</span>

</a>

<a href="upload.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Upload</span>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">HTTP requests</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="39b1d3d3aa5b49999ec0c95cd484c802">

<span data-offset-key="39b1d3d3aa5b49999ec0c95cd484c802:0">A HTTP request is what curl sends to the server when it tells the server what to do. When it wants to get data or send data. All transfers involving HTTP starts with a HTTP request.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b6f167dc088e4ed79b503106e032a844">

<span data-offset-key="b6f167dc088e4ed79b503106e032a844:0">A HTTP request contains a method, a path, HTTP version and a set of request headers. And of course a libcurl using application can tweak all those fields.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="1b17bf130d8e44ddb7a3477c639320d6">

<span data-offset-key="1b17bf130d8e44ddb7a3477c639320d6:0">Request method</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="68d3baf5f8ae437abfe411face094884">

<span data-offset-key="68d3baf5f8ae437abfe411face094884:0">Every HTTP request contains a "method", sometimes referred to as a "verb". It is usually something like GET, HEAD, POST or PUT but there are also more esoteric ones like DELETE, PATCH and OPTIONS.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="74da36f38cd740dbb2343d6839c4441c">

<span data-offset-key="74da36f38cd740dbb2343d6839c4441c:0">Usually when you use libcurl to set up and perform a transfer the specific request method is implied by the options you use. If you just ask for a URL, it means the method will be </span>

<span data-offset-key="74da36f38cd740dbb2343d6839c4441c:1">`GET`</span>

<span data-offset-key="74da36f38cd740dbb2343d6839c4441c:2"> while if you set for example </span>

<span data-offset-key="74da36f38cd740dbb2343d6839c4441c:3">`CURLOPT_POSTFIELDS`</span>

<span data-offset-key="74da36f38cd740dbb2343d6839c4441c:4"> that will make libcurl use the </span>

<span data-offset-key="74da36f38cd740dbb2343d6839c4441c:5">`POST`</span>

<span data-offset-key="74da36f38cd740dbb2343d6839c4441c:6"> method. If you set </span>

<span data-offset-key="74da36f38cd740dbb2343d6839c4441c:7">`CURLOPT_UPLOAD`</span>

<span data-offset-key="74da36f38cd740dbb2343d6839c4441c:8"> to true, libcurl will send a </span>

<span data-offset-key="74da36f38cd740dbb2343d6839c4441c:9">`PUT`</span>

<span data-offset-key="74da36f38cd740dbb2343d6839c4441c:10"> method in its HTTP request and so on. Asking for </span>

<span data-offset-key="74da36f38cd740dbb2343d6839c4441c:11">`CURLOPT_NOBODY`</span>

<span data-offset-key="74da36f38cd740dbb2343d6839c4441c:12"> will make libcurl use </span>

<span data-offset-key="74da36f38cd740dbb2343d6839c4441c:13">`HEAD`</span>

<span data-offset-key="74da36f38cd740dbb2343d6839c4441c:14">.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f83eceefca31416eae33f9b303a4135a">

<span data-offset-key="f83eceefca31416eae33f9b303a4135a:0">However, sometimes those default HTTP methods are not good enough or simply not the ones you want your transfer to use. Then you can instruct libcurl to use the specific method you like with </span>

<span data-offset-key="f83eceefca31416eae33f9b303a4135a:1">`CURLOPT_CUSTOMREQUEST`</span>

<span data-offset-key="f83eceefca31416eae33f9b303a4135a:2">. For example, you want to send a </span>

<span data-offset-key="f83eceefca31416eae33f9b303a4135a:3">`DELETE`</span>

<span data-offset-key="f83eceefca31416eae33f9b303a4135a:4"> method to the URL of your choice:</span>

</span>

</span> curl_easy_setopt(curl, CURLOPT_CUSTOMREQUEST, "DELETE");curl_easy_setopt(curl, CURLOPT_URL, "https://example.com/file.txt");<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ee6fc5c5983e4f86ae351549efe44279">

<span data-offset-key="ee6fc5c5983e4f86ae351549efe44279:0">The CURLOPT_CUSTOMREQUEST setting should only be the single keyword to use as method in the HTTP request line. If you want to change or add additional HTTP request headers, see the following section.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="6f29c8069c89427d8ecf826c72246cde">

<span data-offset-key="6f29c8069c89427d8ecf826c72246cde:0">Customize HTTP request headers</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e502c67c9184434bba7d54663ed7e0b8">

<span data-offset-key="e502c67c9184434bba7d54663ed7e0b8:0">When libcurl issues HTTP requests as part of performing the data transfers you have asked it to, it will of course send them off with a set of HTTP headers that are suitable for fulfilling the task given to it.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="5595a2612e5c46429741be94ae031ea6">

<span data-offset-key="5595a2612e5c46429741be94ae031ea6:0">If just given the URL "</span>

</span>

<a href="http://localhost/file1.txt" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="c56dbb6d53dc481382cf03fdced343c7">

<span data-offset-key="c56dbb6d53dc481382cf03fdced343c7:0">http://localhost/file1.txt</span>

</span>

</a>

<span data-key="433fd2f400a144acbd1d01bdb2bc1a38">

<span data-offset-key="433fd2f400a144acbd1d01bdb2bc1a38:0">", libcurl 7.51.0 would send the following request to the server:</span>

</span>

</span> GET /file1.txt HTTP/1.1Host: localhostAccept: _/_<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="dc77f30835b24f33ac79e22e1503fc22">

<span data-offset-key="dc77f30835b24f33ac79e22e1503fc22:0">If you would instead instruct your application to also set </span>

<span data-offset-key="dc77f30835b24f33ac79e22e1503fc22:1">`CURLOPT_POSTFIELDS`</span>

<span data-offset-key="dc77f30835b24f33ac79e22e1503fc22:2"> to the string "foobar" (6 letters, the quotes only used for visual delimiters here), it would send the following headers:</span>

</span>

</span> POST /file1.txt HTTP/1.1Host: localhostAccept: */*Content-Length: 6Content-Type: application/x-www-form-urlencoded<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="faf398c0dbd242e9b19fa32edf623d84">

<span data-offset-key="faf398c0dbd242e9b19fa32edf623d84:0">If you are not pleased with the default set of headers libcurl sends, the application has the power to add, change or remove headers in the HTTP request.</span>

</span>

</span>

<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="5d363712a8f145978006be8cc8ba1609">

<span data-offset-key="5d363712a8f145978006be8cc8ba1609:0">Add a header</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="064b8a39d12444aeae902fb06519a41e">

<span data-offset-key="064b8a39d12444aeae902fb06519a41e:0">To add a header that would not otherwise be in the request, add it with </span>

<span data-offset-key="064b8a39d12444aeae902fb06519a41e:1">`CURLOPT_HTTPHEADER`</span>

<span data-offset-key="064b8a39d12444aeae902fb06519a41e:2">. Suppose you want a header called </span>

<span data-offset-key="064b8a39d12444aeae902fb06519a41e:3">`Name:`</span>

<span data-offset-key="064b8a39d12444aeae902fb06519a41e:4"> that contains </span>

<span data-offset-key="064b8a39d12444aeae902fb06519a41e:5">`Mr. Smith`</span>

<span data-offset-key="064b8a39d12444aeae902fb06519a41e:6">:</span>

</span>

</span> struct curl_slist _list = NULL;list = curl_slist_append(list, "Name: Mr Smith");curl_easy_setopt(curl, CURLOPT_HTTPHEADER, list);curl_easy_perform(curl);curl_slist_free_all(list); /_ free the list again \*/<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="c9188cc561d44157aedca87616fe11e9">

<span data-offset-key="c9188cc561d44157aedca87616fe11e9:0">Change a header</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a9e29dc3c55e4646b7ef74304c3d32fc">

<span data-offset-key="a9e29dc3c55e4646b7ef74304c3d32fc:0">If one of those default headers are not to your satisfaction you can alter them. Like if you think the default </span>

<span data-offset-key="a9e29dc3c55e4646b7ef74304c3d32fc:1">`Host:`</span>

<span data-offset-key="a9e29dc3c55e4646b7ef74304c3d32fc:2"> header is wrong (even though it is derived from the URL you give libcurl), you can tell libcurl your own:</span>

</span>

</span> struct curl_slist _list = NULL;list = curl_slist_append(list, "Host: Alternative");curl_easy_setopt(curl, CURLOPT_HTTPHEADER, list);curl_easy_perform(curl);curl_slist_free_all(list); /_ free the list again \*/<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="f663712e27074a7689af0d0e0bdb5bb6">

<span data-offset-key="f663712e27074a7689af0d0e0bdb5bb6:0">Remove a header</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8211c7ba199043d8a9f1562575f2c7ab">

<span data-offset-key="8211c7ba199043d8a9f1562575f2c7ab:0">When you think libcurl uses a header in a request that you really think it should not, you can easily tell it to just remove it from the request. Like if you want to take away the </span>

<span data-offset-key="8211c7ba199043d8a9f1562575f2c7ab:1">`Accept:`</span>

<span data-offset-key="8211c7ba199043d8a9f1562575f2c7ab:2"> header. Just provide the header name with nothing to the right sight of the colon:</span>

</span>

</span> struct curl_slist _list = NULL;list = curl_slist_append(list, "Accept:");curl_easy_setopt(curl, CURLOPT_HTTPHEADER, list);curl_easy_perform(curl);curl_slist_free_all(list); /_ free the list again \*/<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="21153cecee6e43b7ae8c2e0b843f9cac">

<span data-offset-key="21153cecee6e43b7ae8c2e0b843f9cac:0">Provide a header without contents</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="5ebb0343dc2c4655a743b3067793f55a">

<span data-offset-key="5ebb0343dc2c4655a743b3067793f55a:0">As you may then have noticed in the above sections, if you try to add a header with no contents on the right side of the colon, it will be treated as a removal instruction and it will instead completely inhibit that header from being sent. If you instead </span>

<span data-offset-key="5ebb0343dc2c4655a743b3067793f55a:1">_truly_</span>

<span data-offset-key="5ebb0343dc2c4655a743b3067793f55a:2"> want to send a header with zero contents on the right side, you need to use a special marker. You must provide the header with a semicolon instead of a proper colon. Like </span>

<span data-offset-key="5ebb0343dc2c4655a743b3067793f55a:3">`Header;`</span>

<span data-offset-key="5ebb0343dc2c4655a743b3067793f55a:4">. So if you want to add a header to the outgoing HTTP request that is just </span>

<span data-offset-key="5ebb0343dc2c4655a743b3067793f55a:5">`Moo:`</span>

<span data-offset-key="5ebb0343dc2c4655a743b3067793f55a:6"> with nothing following the colon, you could write it like:</span>

</span>

</span> struct curl_slist _list = NULL;list = curl_slist_append(list, "Moo;");curl_easy_setopt(curl, CURLOPT_HTTPHEADER, list);curl_easy_perform(curl);curl_slist_free_all(list); /_ free the list again \*/<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="ac8e5eaffd544e2dbe970aaa56ffeb3a">

<span data-offset-key="ac8e5eaffd544e2dbe970aaa56ffeb3a:0">Referrer</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9577d73740cd4a2888296a6db0b0114d">

<span data-offset-key="9577d73740cd4a2888296a6db0b0114d:0">The </span>

<span data-offset-key="9577d73740cd4a2888296a6db0b0114d:1">`Referer:`</span>

<span data-offset-key="9577d73740cd4a2888296a6db0b0114d:2"> header (yes, it is misspelled) is a standard HTTP header that tells the server from which URL the user-agent was directed from when it arrived at the URL it now requests. It is a normal header so you can set it yourself with the </span>

<span data-offset-key="9577d73740cd4a2888296a6db0b0114d:3">`CURLOPT_HEADER`</span>

<span data-offset-key="9577d73740cd4a2888296a6db0b0114d:4"> approach as shown above, or you can use the shortcut known as </span>

<span data-offset-key="9577d73740cd4a2888296a6db0b0114d:5">`CURLOPT_REFERER`</span>

<span data-offset-key="9577d73740cd4a2888296a6db0b0114d:6">. Like this:</span>

</span>

</span> curl_easy_setopt(curl, CURLOPT_REFERER, "https://example.com/fromhere/");curl_easy_perform(curl);<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="0a04c96b65c545f1900d0271fd6f1e30">

<span data-offset-key="0a04c96b65c545f1900d0271fd6f1e30:0">Automatic referrer</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="af805996f49b4d51940707859d2bd01c">

<span data-offset-key="af805996f49b4d51940707859d2bd01c:0">When libcurl is asked to follow redirects itself with the </span>

<span data-offset-key="af805996f49b4d51940707859d2bd01c:1">`CURLOPT_FOLLOWLOCATION`</span>

<span data-offset-key="af805996f49b4d51940707859d2bd01c:2"> option, and you still want to have the </span>

<span data-offset-key="af805996f49b4d51940707859d2bd01c:3">`Referer:`</span>

<span data-offset-key="af805996f49b4d51940707859d2bd01c:4"> header set to the correct previous URL from where it did the redirect, you can ask libcurl to set that by itself:</span>

</span>

</span> curl_easy_setopt(curl, CURLOPT_FOLLOWLOCATION, 1L);curl_easy_setopt(curl, CURLOPT_AUTOREFERER, 1L);curl_easy_setopt(curl, CURLOPT_URL, "https://example.com/redirected.cgi");curl_easy_perform(curl);<a href="responses.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">HTTP responses</span>

<a href="versions.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">HTTP versions</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 8 months ago</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="requests.html#request-method" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Request method</span>

</span>

<a href="requests.html#customize-http-request-headers" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Customize HTTP request headers</span>

</span>

<a href="requests.html#add-a-header" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Add a header</span>

</span>

<a href="requests.html#change-a-header" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Change a header</span>

</span>

<a href="requests.html#remove-a-header" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Remove a header</span>

</span>

<a href="requests.html#provide-a-header-without-contents" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Provide a header without contents</span>

</span>

<a href="requests.html#referrer" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Referrer</span>

</span>

<a href="requests.html#automatic-referrer" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Automatic referrer</span>

</span>
