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

<a href="getinfo.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

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

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Post transfer info</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7ef2ce9620744140a27710bc8c34e6a9">

<span data-offset-key="7ef2ce9620744140a27710bc8c34e6a9:0">Remember how libcurl transfers are associated with an "easy handle"! Each transfer has such a handle and when a transfer is completed, before the handle is cleaned or reused for another transfer, it can be used to extract information from the previous operation.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="3aa68fe6186d4e489c5b6e6435141a5b">

<span data-offset-key="3aa68fe6186d4e489c5b6e6435141a5b:0">Your friend for doing this is called </span>

<span data-offset-key="3aa68fe6186d4e489c5b6e6435141a5b:1">`curl_easy_getinfo()`</span>

<span data-offset-key="3aa68fe6186d4e489c5b6e6435141a5b:2"> and you tell it which specific information you are interested in and it will return that to you if it can.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2d12228eb24a4fd6a5629106ee1bd90c">

<span data-offset-key="2d12228eb24a4fd6a5629106ee1bd90c:0">When you use this function, you pass in the easy handle, which information you want and a pointer to a variable to hold the answer. You must pass in a pointer to a variable of the correct type or you risk that things will go side-ways. These information values are designed to be provided </span>

<span data-offset-key="2d12228eb24a4fd6a5629106ee1bd90c:1">_after_</span>

<span data-offset-key="2d12228eb24a4fd6a5629106ee1bd90c:2"> the transfer is completed.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2881ce6013fe480080d097c6057b30c4">

<span data-offset-key="2881ce6013fe480080d097c6057b30c4:0">The data you receive can be a long, a 'char </span>

<span data-offset-key="2881ce6013fe480080d097c6057b30c4:1">_', a 'struct curl_slist_ </span>

<span data-offset-key="2881ce6013fe480080d097c6057b30c4:2">', a double or a socket.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="17d24947aefd41a1b4808a69cd3ddf11">

<span data-offset-key="17d24947aefd41a1b4808a69cd3ddf11:0">This is how you extract the </span>

<span data-offset-key="17d24947aefd41a1b4808a69cd3ddf11:1">`Content-Type:`</span>

<span data-offset-key="17d24947aefd41a1b4808a69cd3ddf11:2"> value from the previous HTTP transfer:</span>

</span>

</span> CURLcode res;char \*content_type;res = curl_easy_getinfo(curl, CURLINFO_CONTENT_TYPE, &content_type);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="50d7c497075345d4ba9b638709f2f1ed">

<span data-offset-key="50d7c497075345d4ba9b638709f2f1ed:0">If you want to extract the local port number that was used in that connection:</span>

</span>

</span> CURLcode res;long port_number;res = curl_easy_getinfo(curl, CURLINFO_LOCAL_PORT, &port_number);<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="2a5dd339de644f68a2225675c4fb4973">

<span data-offset-key="2a5dd339de644f68a2225675c4fb4973:0">Available information</span>

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

<span data-key="95b83982266446c8b936e0743da2693a">

<span data-offset-key="95b83982266446c8b936e0743da2693a:0">Getinfo option</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">

<span data-key="c547bb7a7a9648e6b7b5c7caddba48e8">

<span data-offset-key="c547bb7a7a9648e6b7b5c7caddba48e8:0">Type</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">

<span data-key="aa801f2d58c643d7817afc5fbe5f6d5e">

<span data-offset-key="aa801f2d58c643d7817afc5fbe5f6d5e:0">Description</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b53c146c404e41d69944f06102c90db3">

<span data-offset-key="b53c146c404e41d69944f06102c90db3:0">CURLINFO_ACTIVESOCKET</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4fd630708ec44e7597622c0f0e987503">

<span data-offset-key="4fd630708ec44e7597622c0f0e987503:0">curl_socket_t</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0c192dcbf9d8408dbe2010b6ac593257">

<span data-offset-key="0c192dcbf9d8408dbe2010b6ac593257:0">The session's active socket</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="3855570f032b4007bca4b7af44d90555">

<span data-offset-key="3855570f032b4007bca4b7af44d90555:0">CURLINFO_APPCONNECT_TIME</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9c28c02a295a49a9a64e53fe0cad3b2e">

<span data-offset-key="9c28c02a295a49a9a64e53fe0cad3b2e:0">double</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4fedf3a2d121472d96ccd6e05b3d30db">

<span data-offset-key="4fedf3a2d121472d96ccd6e05b3d30db:0">Time from start until SSL/SSH handshake completed</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="de8e0c90e5cb4aa991f24c86eba17f15">

<span data-offset-key="de8e0c90e5cb4aa991f24c86eba17f15:0">CURLINFO_APPCONNECT_TIME_T</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f08a0c226efe4b45b122e1d433880eaf">

<span data-offset-key="f08a0c226efe4b45b122e1d433880eaf:0">curl_off_t</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="5469a5a01a0947e38896b7b5a14423ab">

<span data-offset-key="5469a5a01a0947e38896b7b5a14423ab:0">Time from start until SSL/SSH handshake completed (in microseconds)</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="d9bad531f0284bdfacad96bf302f4ada">

<span data-offset-key="d9bad531f0284bdfacad96bf302f4ada:0">CURLINFO_CERTINFO</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ffefe6fa80234e73936fbeefa18540e3">

<span data-offset-key="ffefe6fa80234e73936fbeefa18540e3:0">struct curl_slist \*</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ce271143d71c4f968e455ea7c3cde6fb">

<span data-offset-key="ce271143d71c4f968e455ea7c3cde6fb:0">Certificate chain</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e65b43f0abbc4f40bd1041e4f200130a">

<span data-offset-key="e65b43f0abbc4f40bd1041e4f200130a:0">CURLINFO_CONDITION_UNMET</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="24451beef3ad41b2af8166e32ae1c4a6">

<span data-offset-key="24451beef3ad41b2af8166e32ae1c4a6:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7c085857b4a34262a02ac46841b1b149">

<span data-offset-key="7c085857b4a34262a02ac46841b1b149:0">Whether or not a time conditional was met</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="374162deb8664f47b448cd7728a6df16">

<span data-offset-key="374162deb8664f47b448cd7728a6df16:0">CURLINFO_CONNECT_TIME</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9a02f26d8aec46c7ad890c02c7b29af8">

<span data-offset-key="9a02f26d8aec46c7ad890c02c7b29af8:0">double</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="d351b6071d8b40c68c8b673497ce51f1">

<span data-offset-key="d351b6071d8b40c68c8b673497ce51f1:0">Time from start until remote host or proxy completed</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4c3bc2e6ebdf4939905463655c9ea139">

<span data-offset-key="4c3bc2e6ebdf4939905463655c9ea139:0">CURLINFO_CONNECT_TIME_T</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6bcb08e9bf78404a9412b32f371cc0b6">

<span data-offset-key="6bcb08e9bf78404a9412b32f371cc0b6:0">curl_off_t</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0b8e8d150ab0443d8eb528ee047eb9b4">

<span data-offset-key="0b8e8d150ab0443d8eb528ee047eb9b4:0">Time from start until remote host or proxy completed (in microseconds)</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="3b3fb5f8a03b496698cdab368e78f442">

<span data-offset-key="3b3fb5f8a03b496698cdab368e78f442:0">CURLINFO_CONTENT_LENGTH_DOWNLOAD</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7214590b2eab47f88054bb26705aa20d">

<span data-offset-key="7214590b2eab47f88054bb26705aa20d:0">double</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f9d758cae5c84249bc16642fc2a2aed1">

<span data-offset-key="f9d758cae5c84249bc16642fc2a2aed1:0">Content length from the Content-Length header</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="92e52d3b1dc642978bb2590c511c3e87">

<span data-offset-key="92e52d3b1dc642978bb2590c511c3e87:0">CURLINFO_CONTENT_LENGTH_UPLOAD</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2cf16cb84f8a40a786827d2630ee27a6">

<span data-offset-key="2cf16cb84f8a40a786827d2630ee27a6:0">double</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="69ba25897c8d45f389579cd86ceac05a">

<span data-offset-key="69ba25897c8d45f389579cd86ceac05a:0">Upload size</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="659251cb88fd481e898796f640a8fe7a">

<span data-offset-key="659251cb88fd481e898796f640a8fe7a:0">CURLINFO_CONTENT_TYPE</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="bde94904aabe44f4953ed4a51e4850e8">

<span data-offset-key="bde94904aabe44f4953ed4a51e4850e8:0">char \*</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c6d13eec983a4c8f879fc786bd3351cb">

<span data-offset-key="c6d13eec983a4c8f879fc786bd3351cb:0">Content type from the Content-Type header</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="fb06277f5f7744e6a20c82b88096c07a">

<span data-offset-key="fb06277f5f7744e6a20c82b88096c07a:0">CURLINFO_COOKIELIST</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2f0257ee77ea47f9a370a2a74ed6b9d5">

<span data-offset-key="2f0257ee77ea47f9a370a2a74ed6b9d5:0">struct curl_slist \*</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2a4c59e42faf4cb0bfb1cf8abe591124">

<span data-offset-key="2a4c59e42faf4cb0bfb1cf8abe591124:0">List of all known cookies</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4bda24ae4d534e78b6ba08b5da25dfcb">

<span data-offset-key="4bda24ae4d534e78b6ba08b5da25dfcb:0">CURLINFO_EFFECTIVE_METHOD</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6012f1ab065149a3b9be987be4e1a3cb">

<span data-offset-key="6012f1ab065149a3b9be987be4e1a3cb:0">char \*</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="87b24395e40e4283bbfa875aea49a98e">

<span data-offset-key="87b24395e40e4283bbfa875aea49a98e:0">Last used HTTP request method</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f7714179aa7149d599ff9640e4746ff6">

<span data-offset-key="f7714179aa7149d599ff9640e4746ff6:0">CURLINFO_EFFECTIVE_URL</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="1444fb6a754c4e9a85e82f483b2e89a4">

<span data-offset-key="1444fb6a754c4e9a85e82f483b2e89a4:0">char \*</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e25d72a349de4170a889b170749c952d">

<span data-offset-key="e25d72a349de4170a889b170749c952d:0">Last used URL</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9b711a34eb4a42b19147c6c7bb326bf1">

<span data-offset-key="9b711a34eb4a42b19147c6c7bb326bf1:0">CURLINFO_FILETIME</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9727b87f213e4d5e93e72ee1a616f55e">

<span data-offset-key="9727b87f213e4d5e93e72ee1a616f55e:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="89e9ee55e2bf4734b5d05a404f8090af">

<span data-offset-key="89e9ee55e2bf4734b5d05a404f8090af:0">Remote time of the retrieved document</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="70531ec7f2e3431882e68fe09e305a1d">

<span data-offset-key="70531ec7f2e3431882e68fe09e305a1d:0">CURLINFO_FTP_ENTRY_PATH</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="465456e7803e4fde93370dd63bdc5b48">

<span data-offset-key="465456e7803e4fde93370dd63bdc5b48:0">char \*</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="32cfc4cb458e4b6a9e25ee450a6829ca">

<span data-offset-key="32cfc4cb458e4b6a9e25ee450a6829ca:0">The entry path after logging in to an FTP server</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0ead1036d5bf4e51857afebced3a781c">

<span data-offset-key="0ead1036d5bf4e51857afebced3a781c:0">CURLINFO_HEADER_SIZE</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="5e32a0e968aa46948736c0c737883ff4">

<span data-offset-key="5e32a0e968aa46948736c0c737883ff4:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2812fc36e88743b48f11f420f138a737">

<span data-offset-key="2812fc36e88743b48f11f420f138a737:0">Number of bytes of all headers received</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="57a844e45ddc45d6a921fc7965f554df">

<span data-offset-key="57a844e45ddc45d6a921fc7965f554df:0">CURLINFO_HTTP_CONNECTCODE</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e1e412cab12c4203aad4104a7be4565c">

<span data-offset-key="e1e412cab12c4203aad4104a7be4565c:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="66ca3bc3b95045feb9d2c614fafb71aa">

<span data-offset-key="66ca3bc3b95045feb9d2c614fafb71aa:0">Last proxy CONNECT response code</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="28b81a20fa144e5a9f7401c929b05de3">

<span data-offset-key="28b81a20fa144e5a9f7401c929b05de3:0">CURLINFO_HTTP_VERSION</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="590fb9497fd84754adc90f56bfe57628">

<span data-offset-key="590fb9497fd84754adc90f56bfe57628:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ab7f21c89c5e4791a7a5c64d5d196f28">

<span data-offset-key="ab7f21c89c5e4791a7a5c64d5d196f28:0">The http version used in the connection</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="59ba058fbff04166abd2e96745877679">

<span data-offset-key="59ba058fbff04166abd2e96745877679:0">CURLINFO_HTTPAUTH_AVAIL</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8faadb159453422aad9988688832f984">

<span data-offset-key="8faadb159453422aad9988688832f984:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0a5841fab0104302b2b3bbab39d511ea">

<span data-offset-key="0a5841fab0104302b2b3bbab39d511ea:0">Available HTTP authentication methods (bitmask)</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ef81697955c54f50857258bd8a0afac4">

<span data-offset-key="ef81697955c54f50857258bd8a0afac4:0">CURLINFO_LASTSOCKET</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7bd5f5daec9641bcbd4f96a5b4d304d4">

<span data-offset-key="7bd5f5daec9641bcbd4f96a5b4d304d4:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8a29f04d824f4c06a6afad7f836eb178">

<span data-offset-key="8a29f04d824f4c06a6afad7f836eb178:0">Last socket used</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="d358509fd0934aa2aa4a6a387e6789fb">

<span data-offset-key="d358509fd0934aa2aa4a6a387e6789fb:0">CURLINFO_LOCAL_IP</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e9e64397bc5e488ba891ae5ae7309e6f">

<span data-offset-key="e9e64397bc5e488ba891ae5ae7309e6f:0">char \*</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="048a84f0dddb4a55802071f32bddf870">

<span data-offset-key="048a84f0dddb4a55802071f32bddf870:0">Local-end IP address of last connection</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8adbc57932e74a2d8edcb56961d5c699">

<span data-offset-key="8adbc57932e74a2d8edcb56961d5c699:0">CURLINFO_LOCAL_PORT</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="edfa29c5750642979f67dee8471f9218">

<span data-offset-key="edfa29c5750642979f67dee8471f9218:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="3e86079550fa4f3ba33a5450f4a1fbe7">

<span data-offset-key="3e86079550fa4f3ba33a5450f4a1fbe7:0">Local-end port of last connection</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="709a7aa46742452280f70a5e85d41f2d">

<span data-offset-key="709a7aa46742452280f70a5e85d41f2d:0">CURLINFO_NAMELOOKUP_TIME</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="dbfb2faa1ee04f6690726f965a141df7">

<span data-offset-key="dbfb2faa1ee04f6690726f965a141df7:0">double</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="62aabf998d02404a8fe92b8b952989ff">

<span data-offset-key="62aabf998d02404a8fe92b8b952989ff:0">Time from start until name resolving completed</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9f2abb880cca4f9f8ea5abe734e39768">

<span data-offset-key="9f2abb880cca4f9f8ea5abe734e39768:0">CURLINFO_NAMELOOKUP_TIME_T</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="26c633aed7eb4ab7bc19e75d3933f30b">

<span data-offset-key="26c633aed7eb4ab7bc19e75d3933f30b:0">curl_off_t</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e0409fe051574a508c33f574f61f0a3a">

<span data-offset-key="e0409fe051574a508c33f574f61f0a3a:0">Time from start until name resolving completed (in microseconds)</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="af233b23c8a745089d6f711643bb40d8">

<span data-offset-key="af233b23c8a745089d6f711643bb40d8:0">CURLINFO_NUM_CONNECTS</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="df5d79e652d74c72aafd76727f61ec2a">

<span data-offset-key="df5d79e652d74c72aafd76727f61ec2a:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="670906c30c974b9b82e92ba98118385e">

<span data-offset-key="670906c30c974b9b82e92ba98118385e:0">Number of new successful connections used for previous transfer</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="95e180395c6a4637b16a80eba98634ea">

<span data-offset-key="95e180395c6a4637b16a80eba98634ea:0">CURLINFO_OS_ERRNO</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="936de41e6b9744d58f91cfd1a6b5996f">

<span data-offset-key="936de41e6b9744d58f91cfd1a6b5996f:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="18782560dafb4ce2ae9b0b40c02292cb">

<span data-offset-key="18782560dafb4ce2ae9b0b40c02292cb:0">The errno from the last failure to connect</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="117bcf8086ab4953b844b86bd06cb2ae">

<span data-offset-key="117bcf8086ab4953b844b86bd06cb2ae:0">CURLINFO_PRETRANSFER_TIME</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="faabe4eb5803479293b500a7d4970317">

<span data-offset-key="faabe4eb5803479293b500a7d4970317:0">double</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="df1668dd87bc41cd80c2ede73944caa9">

<span data-offset-key="df1668dd87bc41cd80c2ede73944caa9:0">Time from start until just before the transfer begins</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="dc4921c333d24000a973db5f84ff75b7">

<span data-offset-key="dc4921c333d24000a973db5f84ff75b7:0">CURLINFO_PRETRANSFER_TIME_T</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a2cd787e687f445b81d16b1fbc809e6b">

<span data-offset-key="a2cd787e687f445b81d16b1fbc809e6b:0">curl_off_T</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b5eef4986e7441a6ad8cdaae9b03608c">

<span data-offset-key="b5eef4986e7441a6ad8cdaae9b03608c:0">Time from start until just before the transfer begins (in microseconds)</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2194df1e218640ce961a2d6038746dfc">

<span data-offset-key="2194df1e218640ce961a2d6038746dfc:0">CURLINFO_PRIMARY_IP</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e70936f014594802a1c4d0e72d57a06b">

<span data-offset-key="e70936f014594802a1c4d0e72d57a06b:0">char \*</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a8dc8abb0310447c901fbdabe469bd54">

<span data-offset-key="a8dc8abb0310447c901fbdabe469bd54:0">IP address of the last connection</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4008ee921aa7400b93c0291e18b3fc18">

<span data-offset-key="4008ee921aa7400b93c0291e18b3fc18:0">CURLINFO_PRIMARY_PORT</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2a53dd64cca442328b07e8326326bd78">

<span data-offset-key="2a53dd64cca442328b07e8326326bd78:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="cf2d72749d68421b8ea7fc427cd72a99">

<span data-offset-key="cf2d72749d68421b8ea7fc427cd72a99:0">Port of the last connection</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="3790bf2a648f4f548296cdd330a56189">

<span data-offset-key="3790bf2a648f4f548296cdd330a56189:0">CURLINFO_PRIVATE</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="17529eaebc9444e79e0baf10402e65c5">

<span data-offset-key="17529eaebc9444e79e0baf10402e65c5:0">char \*</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c6adf10961944c28961e4cab15e6a409">

<span data-offset-key="c6adf10961944c28961e4cab15e6a409:0">User's private data pointer</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="73e33f25ad614aa78a57d76f1b318581">

<span data-offset-key="73e33f25ad614aa78a57d76f1b318581:0">CURLINFO_PROTOCOL</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="70867fc6c5d5486d9c400a4f22c965cc">

<span data-offset-key="70867fc6c5d5486d9c400a4f22c965cc:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="55f7960708734412b034ef8737926460">

<span data-offset-key="55f7960708734412b034ef8737926460:0">The protocol used for the connection</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="650f7279e31b4a1199fb5538dfed5800">

<span data-offset-key="650f7279e31b4a1199fb5538dfed5800:0">CURLINFO_PROXY_ERROR</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="eb3b96f4a779435b80328a4490961644">

<span data-offset-key="eb3b96f4a779435b80328a4490961644:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="fc0067af469346d69b2494f43fbc0507">

<span data-offset-key="fc0067af469346d69b2494f43fbc0507:0">Detailed (SOCKS) proxy error if </span>

<span data-offset-key="fc0067af469346d69b2494f43fbc0507:1">

<code class="code-0458e21e" spellcheck="false" data-slate-leaf="true">CURLE_PROXY</code>

</span>

<span data-offset-key="fc0067af469346d69b2494f43fbc0507:2"> was returned from the transfer</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6c213aafaf154db998c644afda02ad71">

<span data-offset-key="6c213aafaf154db998c644afda02ad71:0">CURLINFO_PROXY_SSL_VERIFYRESULT</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8837b1b50e5941e9b21b24f9fe11c5ec">

<span data-offset-key="8837b1b50e5941e9b21b24f9fe11c5ec:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6a213424971f426bb19df6dda4b6650c">

<span data-offset-key="6a213424971f426bb19df6dda4b6650c:0">Proxy certificate verification result</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e31dc0a19bc247f983a46a0e09b3d484">

<span data-offset-key="e31dc0a19bc247f983a46a0e09b3d484:0">CURLINFO_PROXYAUTH_AVAIL</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7fc17d6ca0f44c43b8fdda594b45f61b">

<span data-offset-key="7fc17d6ca0f44c43b8fdda594b45f61b:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8c656cc48efc4c449f66a22232fe16ff">

<span data-offset-key="8c656cc48efc4c449f66a22232fe16ff:0">Available HTTP proxy authentication methods</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b2517d66db44492db6fe9c0c7677dc98">

<span data-offset-key="b2517d66db44492db6fe9c0c7677dc98:0">CURLINFO_REDIRECT_COUNT</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ff17e2e2f9ca4e8f9793a71d779a119b">

<span data-offset-key="ff17e2e2f9ca4e8f9793a71d779a119b:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="dc39b4b80dcb4c4699c3cf4ad529b8f3">

<span data-offset-key="dc39b4b80dcb4c4699c3cf4ad529b8f3:0">Total number of redirects that were followed</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="db7f15adcc4e42bfb78b1a4bd40f0ad3">

<span data-offset-key="db7f15adcc4e42bfb78b1a4bd40f0ad3:0">CURLINFO_REDIRECT_TIME</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4c3156245a5f402e93c202e4833db2a3">

<span data-offset-key="4c3156245a5f402e93c202e4833db2a3:0">double</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ecfd63daa2414d3d8d6b5a83b28ba171">

<span data-offset-key="ecfd63daa2414d3d8d6b5a83b28ba171:0">Time taken for all redirect steps before the final transfer</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="529232d7b00d445493b01ce86a26d82a">

<span data-offset-key="529232d7b00d445493b01ce86a26d82a:0">CURLINFO_REDIRECT_TIME_T</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="1ecc6c41ebb541caac4b99b29472b715">

<span data-offset-key="1ecc6c41ebb541caac4b99b29472b715:0">curl_off_t</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f082e75c19db431bb58f41116b1c0fbe">

<span data-offset-key="f082e75c19db431bb58f41116b1c0fbe:0">Time taken for all redirect steps before the final transfer (in microseconds)</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a02ac0befd654927b55a3145a8bd1ade">

<span data-offset-key="a02ac0befd654927b55a3145a8bd1ade:0">CURLINFO_REDIRECT_URL</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="371330bbb0684d89998015363311d7a0">

<span data-offset-key="371330bbb0684d89998015363311d7a0:0">char \*</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="273de3bfefc643f897266a0261f59f80">

<span data-offset-key="273de3bfefc643f897266a0261f59f80:0">URL a redirect would take you to, had you enabled redirects</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="5b40993aaf4d46f39d973067f2404213">

<span data-offset-key="5b40993aaf4d46f39d973067f2404213:0">CURLINFO_REQUEST_SIZE</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7a5e69e837534c61860eb271f7688ff5">

<span data-offset-key="7a5e69e837534c61860eb271f7688ff5:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="802cd4e2eaa247ddaa4a5b73c388e4a5">

<span data-offset-key="802cd4e2eaa247ddaa4a5b73c388e4a5:0">Number of bytes sent in the issued HTTP requests</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="3daf88d58d6a44f58f80f744bea093d4">

<span data-offset-key="3daf88d58d6a44f58f80f744bea093d4:0">CURLINFO_RESPONSE_CODE</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0c6d2d4f77e74e409c11f7c14ee938fd">

<span data-offset-key="0c6d2d4f77e74e409c11f7c14ee938fd:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7551955042ab4c19b42c61bdc4c66de1">

<span data-offset-key="7551955042ab4c19b42c61bdc4c66de1:0">Last received response code</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="12166edfed7f41a3aaeaaa203a9f20cf">

<span data-offset-key="12166edfed7f41a3aaeaaa203a9f20cf:0">CURLINFO_RETRY_AFTER</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0d9e2765edfb4a52ad8ade1ab376579e">

<span data-offset-key="0d9e2765edfb4a52ad8ade1ab376579e:0">curl_off_t</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="179a0eb9b54e41c588155cf796ca881d">

<span data-offset-key="179a0eb9b54e41c588155cf796ca881d:0">The value from the response </span>

<span data-offset-key="179a0eb9b54e41c588155cf796ca881d:1">

<code class="code-0458e21e" spellcheck="false" data-slate-leaf="true">Retry-After:</code>

</span>

<span data-offset-key="179a0eb9b54e41c588155cf796ca881d:2"> header</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="fc8ba37b46e14d41924474bb5023f78c">

<span data-offset-key="fc8ba37b46e14d41924474bb5023f78c:0">CURLINFO_RTSP_CLIENT_CSEQ</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="effcd3b5efe641dc8602e234146f8c05">

<span data-offset-key="effcd3b5efe641dc8602e234146f8c05:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="28b5d380c92b49de902c0e61272d5fda">

<span data-offset-key="28b5d380c92b49de902c0e61272d5fda:0">RTSP CSeq that will next be used</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="38e57bbe8c504177a3c4ad8aa488f993">

<span data-offset-key="38e57bbe8c504177a3c4ad8aa488f993:0">CURLINFO_RTSP_CSEQ_RECV</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ec6eae236d2f454da7718b1a46e6d2f6">

<span data-offset-key="ec6eae236d2f454da7718b1a46e6d2f6:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="d99c797c321a4a1b9f5b98270e66ae10">

<span data-offset-key="d99c797c321a4a1b9f5b98270e66ae10:0">RTSP CSeq last received</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f304858ba9474246b9139360337664de">

<span data-offset-key="f304858ba9474246b9139360337664de:0">CURLINFO_RTSP_SERVER_CSEQ</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e91a37aeca8a4c17b099bcdaba39d718">

<span data-offset-key="e91a37aeca8a4c17b099bcdaba39d718:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a0f6695aa2514449ac8bcc662be04a6d">

<span data-offset-key="a0f6695aa2514449ac8bcc662be04a6d:0">RTSP CSeq that will next be expected</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="20ca2c6159484024ab656607a1dbdebe">

<span data-offset-key="20ca2c6159484024ab656607a1dbdebe:0">CURLINFO_RTSP_SESSION_ID</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="aa0f8570d2734a59a763c32f3104ebb7">

<span data-offset-key="aa0f8570d2734a59a763c32f3104ebb7:0">char \*</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="190511336be84bf1a47baa042c85ae45">

<span data-offset-key="190511336be84bf1a47baa042c85ae45:0">RTSP session ID</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="88d66eb3caad45be9d84c66125233a7e">

<span data-offset-key="88d66eb3caad45be9d84c66125233a7e:0">CURLINFO_SCHEME</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="90ea82af3c794a55a8892fd039580688">

<span data-offset-key="90ea82af3c794a55a8892fd039580688:0">char \*</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="aa8db0124fd34076ac4a8e22afbd728a">

<span data-offset-key="aa8db0124fd34076ac4a8e22afbd728a:0">The scheme used for the connection</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8a129308e5d14b08bde203f8eb40bc8c">

<span data-offset-key="8a129308e5d14b08bde203f8eb40bc8c:0">CURLINFO_SIZE_DOWNLOAD</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f0466d15729a478482773d5a7aba7ceb">

<span data-offset-key="f0466d15729a478482773d5a7aba7ceb:0">double</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4f30f4587ddc454db750e42777f5ee27">

<span data-offset-key="4f30f4587ddc454db750e42777f5ee27:0">Number of bytes downloaded</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7538114d739745eb9ae89be96c11b6bd">

<span data-offset-key="7538114d739745eb9ae89be96c11b6bd:0">CURLINFO_SIZE_UPLOAD</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="09f48377f28c4b37a7ee2cb35bf52b19">

<span data-offset-key="09f48377f28c4b37a7ee2cb35bf52b19:0">double</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="51e15645d9db4cf8a80487a932e11b36">

<span data-offset-key="51e15645d9db4cf8a80487a932e11b36:0">Number of bytes uploaded</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="756d3c7c47514c288e79ad87ca3dba5d">

<span data-offset-key="756d3c7c47514c288e79ad87ca3dba5d:0">CURLINFO_SPEED_DOWNLOAD</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c412651d70584f27870d435dc83a41b8">

<span data-offset-key="c412651d70584f27870d435dc83a41b8:0">double</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="025bfa801b944facbef6ec3a6630435d">

<span data-offset-key="025bfa801b944facbef6ec3a6630435d:0">Average download speed</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c9f1e38469224f2a8e84687cbf3a54d0">

<span data-offset-key="c9f1e38469224f2a8e84687cbf3a54d0:0">CURLINFO_SPEED_UPLOAD</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="fe95ad4b22e446428c61b428047d4dd5">

<span data-offset-key="fe95ad4b22e446428c61b428047d4dd5:0">double</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7809940b7bf64bab9ba6367d0231f415">

<span data-offset-key="7809940b7bf64bab9ba6367d0231f415:0">Average upload speed</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7f39fb3dd56d4903a56c6ba31fa6e324">

<span data-offset-key="7f39fb3dd56d4903a56c6ba31fa6e324:0">CURLINFO_SSL_ENGINES</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6ff299ab392f4309822f396765f84f84">

<span data-offset-key="6ff299ab392f4309822f396765f84f84:0">struct curl_slist \*</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ca7b4285ac2a483db0aa9c4806c3c6a0">

<span data-offset-key="ca7b4285ac2a483db0aa9c4806c3c6a0:0">A list of OpenSSL crypto engines</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="69eb106f90394d4a8e065994f407367f">

<span data-offset-key="69eb106f90394d4a8e065994f407367f:0">CURLINFO_SSL_VERIFYRESULT</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c0972bacfad54372ac8b9823ca95b1db">

<span data-offset-key="c0972bacfad54372ac8b9823ca95b1db:0">long</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4b697e0ad3d5456ea2038df28a4d6cec">

<span data-offset-key="4b697e0ad3d5456ea2038df28a4d6cec:0">Certificate verification result</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0f93e6d9876946ddb3913b739ec4851b">

<span data-offset-key="0f93e6d9876946ddb3913b739ec4851b:0">CURLINFO_STARTTRANSFER_TIME</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7494178f7139405da5bbd676cfdb7cf4">

<span data-offset-key="7494178f7139405da5bbd676cfdb7cf4:0">double</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8cd9f9b1283f4895a65c84d5807bd3a5">

<span data-offset-key="8cd9f9b1283f4895a65c84d5807bd3a5:0">Time from start until just when the first byte is received</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a336f77aa24743388cbde2a6e49201dc">

<span data-offset-key="a336f77aa24743388cbde2a6e49201dc:0">CURLINFO_STARTTRANSFER_TIME_T</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="5470686f9e35489a81155dc6c9375098">

<span data-offset-key="5470686f9e35489a81155dc6c9375098:0">curl_off_t</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0234d7f5f2f1408d8ef672fc83452036">

<span data-offset-key="0234d7f5f2f1408d8ef672fc83452036:0">Time from start until just when the first byte is received (in microseconds)</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="044ae5d5898e43faaea004d4936a7188">

<span data-offset-key="044ae5d5898e43faaea004d4936a7188:0">CURLINFO_TLS_SSL_PTR</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="723c45693ba24f17a575b2904b3d30d2">

<span data-offset-key="723c45693ba24f17a575b2904b3d30d2:0">struct curl_slist \*</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="1cb32ddf1911480e8c51900b5121b990">

<span data-offset-key="1cb32ddf1911480e8c51900b5121b990:0">TLS session info that can be used for further processing</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="even">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="1213a4af43bd4a659db768ec6f6565e2">

<span data-offset-key="1213a4af43bd4a659db768ec6f6565e2:0">CURLINFO_TOTAL_TIME</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e412dda3f3f64327ada640c9f8a595cd">

<span data-offset-key="e412dda3f3f64327ada640c9f8a595cd:0">double</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e5060f4156824279800f939daadb9484">

<span data-offset-key="e5060f4156824279800f939daadb9484:0">Total time of previous transfer</span>

</span>

</span>

</p>

</td>

</tr>

<tr class="odd">

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8028aded05454a2ca2bc78ef28ecbfe6">

<span data-offset-key="8028aded05454a2ca2bc78ef28ecbfe6:0">CURLINFO_TOTAL_TIME_T</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="3541734360ef4acf87386cf8bd5feb68">

<span data-offset-key="3541734360ef4acf87386cf8bd5feb68:0">curl_off_t</span>

</span>

</span>

</p>

</td>

<td style="text-align: left;">

<p>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2e40360fbc03472caf44241af40ad639">

<span data-offset-key="2e40360fbc03472caf44241af40ad639:0">Total time of previous transfer (in microseconds)</span>

</span>

</span>

</p>

</td>

</tr>

</tbody>

</table>

<a href="proxies.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Proxies</span>

<a href="sharing.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Share data between handles</span>
