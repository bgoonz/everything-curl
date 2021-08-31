<a href="write.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Write data</span>
</a>
<a href="header.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Header data</span>
</a>
<a href="sshkey.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">SSH key</span>
</a># <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Header data</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="15d1553a0d5545a78dcd38431a5272ff">
<span data-offset-key="15d1553a0d5545a78dcd38431a5272ff:0">The header callback is set with </span>
<span data-offset-key="15d1553a0d5545a78dcd38431a5272ff:1">`CURLOPT_HEADERFUNCTION`</span>
<span data-offset-key="15d1553a0d5545a78dcd38431a5272ff:2">:</span>
</span>
</span>    curl_easy_setopt(handle, CURLOPT_HEADERFUNCTION, header_callback);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="c506d581dccc4dceb9804d45d06f7453">
<span data-offset-key="c506d581dccc4dceb9804d45d06f7453:0">The </span>
<span data-offset-key="c506d581dccc4dceb9804d45d06f7453:1">`header_callback`</span>
<span data-offset-key="c506d581dccc4dceb9804d45d06f7453:2"> function must match this prototype:</span>
</span>
</span>    size_t header_callback(char *ptr, size_t size, size_t nmemb, void *userdata);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="c78e5c696b394aea9c83420fbb13a7dc">
<span data-offset-key="c78e5c696b394aea9c83420fbb13a7dc:0">This callback function gets called by libcurl as soon as a header has been received. </span>
<span data-offset-key="c78e5c696b394aea9c83420fbb13a7dc:1">_ptr_</span>
<span data-offset-key="c78e5c696b394aea9c83420fbb13a7dc:2"> points to the delivered data, and the size of that data is </span>
<span data-offset-key="c78e5c696b394aea9c83420fbb13a7dc:3">_size_</span>
<span data-offset-key="c78e5c696b394aea9c83420fbb13a7dc:4"> multiplied with </span>
<span data-offset-key="c78e5c696b394aea9c83420fbb13a7dc:5">_nmemb_</span>
<span data-offset-key="c78e5c696b394aea9c83420fbb13a7dc:6">. libcurl buffers headers and delivers only "full" headers, one by one, to this callback.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="39605924e9c841d6a09df78edea77c19">
<span data-offset-key="39605924e9c841d6a09df78edea77c19:0">The data passed to this function will not be zero terminated! You cannot, for example, use printf's </span>
<span data-offset-key="39605924e9c841d6a09df78edea77c19:1">`%s`</span>
<span data-offset-key="39605924e9c841d6a09df78edea77c19:2"> operator to display the contents nor strcpy to copy it.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="ac98f13110964ca48c13b0cc7c78bf15">
<span data-offset-key="ac98f13110964ca48c13b0cc7c78bf15:0">This callback should return the number of bytes actually taken care of. If that number differs from the number passed to your callback function, it signals an error condition to the library. This will cause the transfer to abort and the libcurl function used will return </span>
<span data-offset-key="ac98f13110964ca48c13b0cc7c78bf15:1">`CURLE_WRITE_ERROR`</span>
<span data-offset-key="ac98f13110964ca48c13b0cc7c78bf15:2">.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="fabb88d198ad4aaa98a764295b2d0b26">
<span data-offset-key="fabb88d198ad4aaa98a764295b2d0b26:0">The user pointer passed in to the callback in the </span>
<span data-offset-key="fabb88d198ad4aaa98a764295b2d0b26:1">_userdata_</span>
<span data-offset-key="fabb88d198ad4aaa98a764295b2d0b26:2"> argument is set with </span>
<span data-offset-key="fabb88d198ad4aaa98a764295b2d0b26:3">`CURLOPT_HEADERDATA`</span>
<span data-offset-key="fabb88d198ad4aaa98a764295b2d0b26:4">:</span>
</span>
</span>    curl_easy_setopt(handle, CURLOPT_HEADERDATA, custom_pointer);<a href="progress.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">
</a>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Progress information</span>
<a href="debug.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">
</a>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Debug</span>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>
