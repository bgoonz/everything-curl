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

<a href="versions.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP versions</span></a>

<a href="ranges.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP ranges</span></a>

<a href="auth.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP authentication</span></a>

<a href="cookies.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Cookies with libcurl</span></a>

<a href="download.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Download</span></a>

<a href="upload.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Upload</span></a>

<a href="../bindings.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Bindings</span></a>

<a href="../internals.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">libcurl internals</span></a>

<a href="../bookindex.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f"></span></a>





# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Download</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2"></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="f6ff1302addf493eacb0256ab0aff611"><span data-offset-key="f6ff1302addf493eacb0256ab0aff611:0">The GET method is the default method libcurl uses when a HTTP URL is requested and no particular other method is asked for. It asks the server for a particular resource—the standard HTTP download request:</span></span></span>

    easy = curl_easy_init();curl_easy_setopt(easy, CURLOPT_URL, "http://example.com/");curl_easy_perform(easy);

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="871383ac47aa481d85f35ffa877329cf"><span data-offset-key="871383ac47aa481d85f35ffa877329cf:0">Since options set in an easy handle are sticky and remain until changed, there may be times when you have asked for another request method than GET and then want to switch back to GET again for a subsequent request. For this purpose, there's the </span><span data-offset-key="871383ac47aa481d85f35ffa877329cf:1">`CURLOPT_HTTPGET`</span><span data-offset-key="871383ac47aa481d85f35ffa877329cf:2"> option:</span></span></span>

    curl_easy_setopt(easy, CURLOPT_HTTPGET, 1L);

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="1caa475410e2454cb0d05a5134248404"><span data-offset-key="1caa475410e2454cb0d05a5134248404:0">Download headers too</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="eae44d66563a4336b0b281a14210b1fb"><span data-offset-key="eae44d66563a4336b0b281a14210b1fb:0">A HTTP transfer also includes a set of response headers. Response headers are metadata associated with the actual payload, called the response body. All downloads will get a set of headers too, but when using libcurl you can select whether you want to have them downloaded (seen) or not.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="e58200d7429c49b2b61b8729ed2d034e"><span data-offset-key="e58200d7429c49b2b61b8729ed2d034e:0">You can ask libcurl to pass on the headers to the same "stream" as the regular body is, by using </span><span data-offset-key="e58200d7429c49b2b61b8729ed2d034e:1">`CURLOPT_HEADER`</span><span data-offset-key="e58200d7429c49b2b61b8729ed2d034e:2">:</span></span></span>

    easy = curl_easy_init();curl_easy_setopt(easy, CURLOPT_HEADER, 1L);curl_easy_setopt(easy, CURLOPT_URL, "http://example.com/");curl_easy_perform(easy);

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="418104d89fde43a49f87c202ddcd266c"><span data-offset-key="418104d89fde43a49f87c202ddcd266c:0">Or you can opt to store the headers in a separate download file, by relying on the default behaviors of the </span></span><a href="../libcurl/callbacks/write.html" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="afb7bd71e8f2423f8114c2ba7b9c4f94"><span data-offset-key="afb7bd71e8f2423f8114c2ba7b9c4f94:0">write</span></span></a><span data-key="64d8c984a1264143b4392252e86bd7bc"><span data-offset-key="64d8c984a1264143b4392252e86bd7bc:0"> and </span></span><a href="../libcurl/callbacks/header.html" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="2250e495e4394e5880df410277dea99f"><span data-offset-key="2250e495e4394e5880df410277dea99f:0">header callbacks</span></span></a><span data-key="23f177d7526a4fec9d0254b95eb0394e"><span data-offset-key="23f177d7526a4fec9d0254b95eb0394e:0">:</span></span></span>

    easy = curl_easy_init();FILE *file = fopen("headers", "wb");curl_easy_setopt(easy, CURLOPT_HEADERDATA, file);curl_easy_setopt(easy, CURLOPT_URL, "http://example.com/");curl_easy_perform(easy);fclose(file);

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="67c1a54fff984564bba7468dcaf5fd11"><span data-offset-key="67c1a54fff984564bba7468dcaf5fd11:0">If you only want to casually browse the headers, you may even be happy enough with just setting verbose mode while developing as that will show both outgoing and incoming headers sent to stderr:</span></span></span>

    curl_easy_setopt(easy, CURLOPT_VERBOSE, 1L);

<a href="cookies.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674"></a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Cookies with libcurl</span>

<a href="upload.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42"></a>


<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Upload</span>



<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>


