<a href="responses.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP responses</span>

</a>

<a href="requests.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

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

<a href="upload.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Upload</span>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Upload</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4b9465b99506453a9a19822dd6b98f21">

<span data-offset-key="4b9465b99506453a9a19822dd6b98f21:0">Uploads over HTTP can be done in many different ways and it is important to notice the differences. They can use different methods, like POST or PUT, and when using POST the body formatting can differ.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9760345fba2f4f7584f00a3865e0e164">

<span data-offset-key="9760345fba2f4f7584f00a3865e0e164:0">In addition to those HTTP differences, libcurl offers different ways to provide the data to upload.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="7eda40d20b8d4d0fb71d417137ea44d2">

<span data-offset-key="7eda40d20b8d4d0fb71d417137ea44d2:0">HTTP POST</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b92b2147fe1c441b9f979680d4719213">

<span data-offset-key="b92b2147fe1c441b9f979680d4719213:0">POST is typically the HTTP method to pass data to a remote web application. A common way to do that in browsers is by filling in a HTML form and pressing submit. It is the standard way for a HTTP request to pass on data to the server. With libcurl you normally provide that data as a pointer and a length:</span>

</span>

</span>    curl_easy_setopt(easy, CURLOPT_POSTFIELDS, dataptr);curl_easy_setopt(easy, CURLOPT_POSTFIELDSIZE, (long)datalength);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="febc65f65a32408495d883ecd0195ffe">

<span data-offset-key="febc65f65a32408495d883ecd0195ffe:0">Or you tell libcurl that it is a post but would prefer to have libcurl instead get the data by using the regular </span>

</span>

<a href="https://github.com/bagder/everything-curl/tree/ac82fad6784dcc3f536df03d1d97bad1849a59c8/libcurl-http/callback-read.md" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="311ab0783b8a4f48b7093b944ca706af">

<span data-offset-key="311ab0783b8a4f48b7093b944ca706af:0">read callback</span>

</span>

</a>

<span data-key="4d6a2bccf01f4ffb83e394b659e368df">

<span data-offset-key="4d6a2bccf01f4ffb83e394b659e368df:0">:</span>

</span>

</span>    curl_easy_setopt(easy, CURLOPT_POST, 1L);curl_easy_setopt(easy, CURLOPT_READFUNCTION, read_callback);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="797454268df34b4e9fb478e0fff94f9f">

<span data-offset-key="797454268df34b4e9fb478e0fff94f9f:0">This "normal" POST will also set the request header </span>

<span data-offset-key="797454268df34b4e9fb478e0fff94f9f:1">`Content-Type: application/x-www-form-urlencoded`</span>

<span data-offset-key="797454268df34b4e9fb478e0fff94f9f:2">.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="472e4c4fdf2a4012af7d8e6a6aaa30b1">

<span data-offset-key="472e4c4fdf2a4012af7d8e6a6aaa30b1:0">HTTP multipart formposts</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="242c9ddc3c80465db240edcf1db7c3e1">

<span data-offset-key="242c9ddc3c80465db240edcf1db7c3e1:0">A multipart formpost is still using the same HTTP method POST; the difference is only in the formatting of the request body. A multipart formpost is a series of separate "parts", separated by MIME-style boundary strings. There's no limit to how many parts you can send.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6c61c0e6399843c0b0d6eed8d413dc4c">

<span data-offset-key="6c61c0e6399843c0b0d6eed8d413dc4c:0">Each such part has a name, a set of headers and a few other properties.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8d5b26b5d185421a98a28983ba61bda7">

<span data-offset-key="8d5b26b5d185421a98a28983ba61bda7:0">libcurl offers a set of convenience functions for constructing such a series of parts and to send that off to the server, all prefixed with </span>

<span data-offset-key="8d5b26b5d185421a98a28983ba61bda7:1">`curl_mime`</span>

<span data-offset-key="8d5b26b5d185421a98a28983ba61bda7:2">. Create a multipart post and for each part in the data you set the name, the data and perhaps additional meta-data. A very basic setup might look like this:</span>

</span>

</span>    /* Create the form */form = curl_mime_init(curl);​/* Fill in the file upload field */field = curl_mime_addpart(form);curl_mime_name(field, "sendfile");curl_mime_filedata(field, "photo.jpg");<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="293b2b28b35e4a05ae4df35b2aa5aa8c">

<span data-offset-key="293b2b28b35e4a05ae4df35b2aa5aa8c:0">Then you pass that post to libcurl like this:</span>

</span>

</span>    curl_easy_setopt(easy, CURLOPT_MIMEPOST, form);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0b6e0b6c89ef4ac6be5082fc5fee776f">

<span data-offset-key="0b6e0b6c89ef4ac6be5082fc5fee776f:0">(</span>

<span data-offset-key="0b6e0b6c89ef4ac6be5082fc5fee776f:1">`curl_formadd`</span>

<span data-offset-key="0b6e0b6c89ef4ac6be5082fc5fee776f:2"> is the former API to build multi-part fromposts with but we no longer recommend using that)</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="db441dcc895749cd8bf1267f785205fc">

<span data-offset-key="db441dcc895749cd8bf1267f785205fc:0">HTTP PUT</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="77a91fa358644f38ae745f0c4eee01af">

<span data-offset-key="77a91fa358644f38ae745f0c4eee01af:0">A PUT with libcurl will assume you pass the data to it using the read callback, as that is the typical "file upload" pattern libcurl uses and provides. You set the callback, you ask for PUT (by asking for </span>

<span data-offset-key="77a91fa358644f38ae745f0c4eee01af:1">`CURLOPT_UPLOAD`</span>

<span data-offset-key="77a91fa358644f38ae745f0c4eee01af:2">), you set the size of the upload and you set the URL to the destination:</span>

</span>

</span>    curl_easy_setopt(easy, CURLOPT_UPLOAD, 1L);curl_easy_setopt(easy, CURLOPT_INFILESIZE_LARGE, (curl_off_t) size);curl_easy_setopt(easy, CURLOPT_READFUNCTION, read_callback);curl_easy_setopt(easy, CURLOPT_URL, "https://example.com/handle/put");<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="cb96fd5146774c14a652c911d860c35c">

<span data-offset-key="cb96fd5146774c14a652c911d860c35c:0">If you for some reason do not know the size of the upload before the transfer starts, and you are using HTTP 1.1 you can add a </span>

<span data-offset-key="cb96fd5146774c14a652c911d860c35c:1">`Transfer-Encoding: chunked`</span>

<span data-offset-key="cb96fd5146774c14a652c911d860c35c:2"> header with </span>

</span>

<a href="https://github.com/bagder/everything-curl/tree/ac82fad6784dcc3f536df03d1d97bad1849a59c8/libcurl-http/libcurl-http-requests.md" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="88250193cb614439953fb6c0fb8bf154">

<span data-offset-key="88250193cb614439953fb6c0fb8bf154:0">CURLOPT_HTTPHEADER</span>

</span>

</a>

<span data-key="b1ca05615fa34423a2541ed5ff50c944">

<span data-offset-key="b1ca05615fa34423a2541ed5ff50c944:0">. For HTTP 1.0 you must provide the size before hand and for HTTP 2 and later, neither the size nor the extra header is needed.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="c8d706d571ba4b7784ba3f21751bc718">

<span data-offset-key="c8d706d571ba4b7784ba3f21751bc718:0">Expect: headers</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7cde546ea03e42efa4f580bb4faef3d8">

<span data-offset-key="7cde546ea03e42efa4f580bb4faef3d8:0">When doing HTTP uploads using HTTP 1.1, libcurl will insert an </span>

<span data-offset-key="7cde546ea03e42efa4f580bb4faef3d8:1">`Expect: 100-continue`</span>

<span data-offset-key="7cde546ea03e42efa4f580bb4faef3d8:2"> header in some circumstances. This header offers the server a way to reject the transfer early and save the client from having to send a lot of data in vain before the server gets a chance to decline.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7b4707648876413a9a3e131ed1880e8d">

<span data-offset-key="7b4707648876413a9a3e131ed1880e8d:0">The header is added by libcurl if HTTP uploading is done with </span>

<span data-offset-key="7b4707648876413a9a3e131ed1880e8d:1">`CURLOPT_UPLOAD`</span>

<span data-offset-key="7b4707648876413a9a3e131ed1880e8d:2"> or if it is asked to do a HTTP POST for which the body size is either unknown or known to be larger than 1024 bytes.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6658ace119324949900014de14687e5e">

<span data-offset-key="6658ace119324949900014de14687e5e:0">A libcurl-using client can explicitly disable the use of the </span>

<span data-offset-key="6658ace119324949900014de14687e5e:1">`Expect:`</span>

<span data-offset-key="6658ace119324949900014de14687e5e:2"> header with the </span>

</span>

<a href="https://github.com/bagder/everything-curl/tree/ac82fad6784dcc3f536df03d1d97bad1849a59c8/libcurl-http/libcurl-http-requests.md" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="de4d5ef20244428692b5b64393188afe">

<span data-offset-key="de4d5ef20244428692b5b64393188afe:0">CURLOPT_HTTPHEADER</span>

</span>

</a>

<span data-key="bd13b993bd8b4b4ebc056c0667be4822">

<span data-offset-key="bd13b993bd8b4b4ebc056c0667be4822:0"> option.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="42315ab3dc1249deab71fe17bb43d929">

<span data-offset-key="42315ab3dc1249deab71fe17bb43d929:0">This header is not used with HTTP/2 or HTTP/3.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="6a086749ec804848b737771738bf4cda">

<span data-offset-key="6a086749ec804848b737771738bf4cda:0">Uploads also downloads</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="57a9c00c606f49f39a831319415ba85f">

<span data-offset-key="57a9c00c606f49f39a831319415ba85f:0">HTTP is a protocol that can respond with contents back even when you upload data to it - it is up to the server to decide. The response data may even start getting sent back to the client before the upload has completed.</span>

</span>

</span>

<a href="download.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Download</span>

<a href="../bindings.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Bindings</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="upload.html#http-post" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">HTTP POST</span>

</span>

<a href="upload.html#http-multipart-formposts" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">HTTP multipart formposts</span>

</span>

<a href="upload.html#http-put" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">HTTP PUT</span>

</span>

<a href="upload.html#expect-headers" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Expect: headers</span>

</span>

<a href="upload.html#uploads-also-downloads" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Uploads also downloads</span>

</span>
