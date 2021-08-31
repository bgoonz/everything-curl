<a href="responses.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

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

</a>

<a href="cookies.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="download.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="upload.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Upload</span>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">HTTP responses</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a6a3f7c148af426ebd8617e73c472f76">

<span data-offset-key="a6a3f7c148af426ebd8617e73c472f76:0">Every HTTP request includes a HTTP response. A HTTP response is a set of metadata and a response body, where the body can occasionally be zero bytes and thus nonexistent. A HTTP response will however always have response headers.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="56f9fecbcf9a49c7902f274c277290d9">

<span data-offset-key="56f9fecbcf9a49c7902f274c277290d9:0">The response body will be passed to the </span>

</span>

<a href="../libcurl/callbacks/write.html" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="2689f3d8f1274835abf7627e691fba10">

<span data-offset-key="2689f3d8f1274835abf7627e691fba10:0">write callback</span>

</span>

</a>

<span data-key="2f6bf47de30343c7a866e4d265b7a749">

<span data-offset-key="2f6bf47de30343c7a866e4d265b7a749:0"> and the response headers to the </span>

</span>

<a href="../libcurl/callbacks/header.html" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="5025ff886612473dafa337b74a878918">

<span data-offset-key="5025ff886612473dafa337b74a878918:0">header callback</span>

</span>

</a>

<span data-key="8ecadaabbfd04c108177731d0dd4e6bc">

<span data-offset-key="8ecadaabbfd04c108177731d0dd4e6bc:0">, but sometimes an application just want to know the size of the data.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7bb7fe21fdfd4277bc98e0c620feedf5">

<span data-offset-key="7bb7fe21fdfd4277bc98e0c620feedf5:0">The size of a response </span>

<span data-offset-key="7bb7fe21fdfd4277bc98e0c620feedf5:1">_as told by the server headers_</span>

<span data-offset-key="7bb7fe21fdfd4277bc98e0c620feedf5:2"> can be extracted with </span>

<span data-offset-key="7bb7fe21fdfd4277bc98e0c620feedf5:3">`curl_easy_getinfo()`</span>

<span data-offset-key="7bb7fe21fdfd4277bc98e0c620feedf5:4"> like this:</span>

</span>

</span>    double size;curl_easy_getinfo(curl, CURLINFO_CONTENT_LENGTH_DOWNLOAD, &size);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="93beb1c59e5c45f79f030bd54db7232b">

<span data-offset-key="93beb1c59e5c45f79f030bd54db7232b:0">If you can wait until after the transfer is already done, which also is a more reliable way since not all URLs will provide the size up front (like for example for servers that generate content on demand) you can instead ask for the amount of downloaded data in the most recent transfer.</span>

</span>

</span>    double size;curl_easy_getinfo(curl, CURLINFO_SIZE_DOWNLOAD, &size);<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="d28140fbd98e4e5881a6e500382a1865">

<span data-offset-key="d28140fbd98e4e5881a6e500382a1865:0">HTTP response code</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4805e1f92e214979bfd37a82959b324f">

<span data-offset-key="4805e1f92e214979bfd37a82959b324f:0">Every HTTP response starts off with a single line that contains the HTTP response code. It is a three digit number that contains the server's idea of the status for the request. The numbers are detailed in the HTTP standard specifications but they are divided into ranges that work like this:</span>

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

<span data-key="0a9cb95ae64046808969aa90e291d38e">

<span data-offset-key="0a9cb95ae64046808969aa90e291d38e:0">Code</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">

<span data-key="305d4e1c4e0a4381bafc2a0e24567209">

<span data-offset-key="305d4e1c4e0a4381bafc2a0e24567209:0">Meaning</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b8995889f5414055b7aec94dfe4636ce">

<span data-offset-key="b8995889f5414055b7aec94dfe4636ce:0">1xx</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7a2551a3bed647ffa61ea90998d8301d">

<span data-offset-key="7a2551a3bed647ffa61ea90998d8301d:0">Transient code, a new one follows</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6ac514f0c45b4f96b14bf84857c23b38">

<span data-offset-key="6ac514f0c45b4f96b14bf84857c23b38:0">2xx</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e9a547ef53da41b397e0e18f9a6fdab4">

<span data-offset-key="e9a547ef53da41b397e0e18f9a6fdab4:0">Things are OK</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8b584b9c0185407c85337b64d76e4135">

<span data-offset-key="8b584b9c0185407c85337b64d76e4135:0">3xx</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="fa2df1a907294e25bf994d0b8d53e5e5">

<span data-offset-key="fa2df1a907294e25bf994d0b8d53e5e5:0">The content is somewhere else</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="3405535392b9454a98133c29024c1227">

<span data-offset-key="3405535392b9454a98133c29024c1227:0">4xx</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2d6fd56389414fe983de8ba6629aa8cf">

<span data-offset-key="2d6fd56389414fe983de8ba6629aa8cf:0">Failed because of a client problem</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f257c1cce2174d9185dfc2864a10a658">

<span data-offset-key="f257c1cce2174d9185dfc2864a10a658:0">5xx</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="906519d366e842718ff6b139cebfaf3b">

<span data-offset-key="906519d366e842718ff6b139cebfaf3b:0">Failed because of a server problem</span>

</span>

</span>

</p>

</td>

</tr>

</tbody>

</table>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f2359815671f49fcab73068987ce01ac">

<span data-offset-key="f2359815671f49fcab73068987ce01ac:0">You can extract the response code after a transfer like this</span>

</span>

</span>    long code;curl_easy_getinfo(curl, CURLINFO_RESPONSE_CODE, &code);<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="6703898ada3340f3a7df2efd39d447dd">

<span data-offset-key="6703898ada3340f3a7df2efd39d447dd:0">About HTTP response code "errors"</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="48a7120d58694f8da8d1188889532936">

<span data-offset-key="48a7120d58694f8da8d1188889532936:0">While the response code numbers can include numbers (in the 4xx and 5xx ranges) which the server uses to signal that there was an error processing the request, it is important to realize that this will not cause libcurl to return an error.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="32f02cea10424fd98dfb0c6d8b4320c7">

<span data-offset-key="32f02cea10424fd98dfb0c6d8b4320c7:0">When libcurl is asked to perform a HTTP transfer it will return an error if that HTTP transfer fails. However, getting a HTTP 404 or the like back is not a problem for libcurl. It is not a HTTP transfer error. A user might be writing a client for testing a server's HTTP responses.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b3834928f8014040b16640320f927b31">

<span data-offset-key="b3834928f8014040b16640320f927b31:0">If you insist on curl treating HTTP response codes from 400 and up as errors, libcurl offers the </span>

<span data-offset-key="b3834928f8014040b16640320f927b31:1">`CURLOPT_FAILONERROR`</span>

<span data-offset-key="b3834928f8014040b16640320f927b31:2"> option that if set instructs curl to return </span>

<span data-offset-key="b3834928f8014040b16640320f927b31:3">`CURLE_HTTP_RETURNED_ERROR`</span>

<span data-offset-key="b3834928f8014040b16640320f927b31:4"> in this case. It will then return error as soon as possible and not deliver the response body.</span>

</span>

</span>

<a href="../libcurl-http.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">HTTP with libcurl</span>

<a href="requests.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">HTTP requests</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 12 months ago</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="responses.html#http-response-code" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">HTTP response code</span>

</span>

<a href="responses.html#about-http-response-code-errors" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">About HTTP response code "errors"</span>

</span>
