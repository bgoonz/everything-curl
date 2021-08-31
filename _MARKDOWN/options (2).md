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

<a href="getinfo.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

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

<a href="options/tlsoptions.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">TLS options</span>

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

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">curl easy options</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="106bfbf4e8e84983a1947d26e346b841">

<span data-offset-key="106bfbf4e8e84983a1947d26e346b841:0">You set options in the easy handle to control how that transfer is going to be done, or in some cases you can actually set options and modify the transfer's behavior while it is in progress. You set options with </span>

<span data-offset-key="106bfbf4e8e84983a1947d26e346b841:1">`curl_easy_setopt()`</span>

<span data-offset-key="106bfbf4e8e84983a1947d26e346b841:2"> and you provide the handle, the option you want to set and the argument to the option. All options take exactly one argument and you must always pass exactly three parameters to the curl_easy_setopt() calls.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f74659d2b69442df8ccd43fb24ad24a9">

<span data-offset-key="f74659d2b69442df8ccd43fb24ad24a9:0">Since the curl_easy_setopt() call accepts several hundred different options and the various options accept a variety of different types of arguments, it is important to read up on the specifics and provide exactly the argument type the specific option supports and expects. Passing in the wrong type can lead to unexpected side-effects or hard to understand hiccups.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7a388ef98bcf47fd8f832876af90c50d">

<span data-offset-key="7a388ef98bcf47fd8f832876af90c50d:0">The perhaps most important option that every transfer needs, is the URL. libcurl cannot perform a transfer without knowing which URL it concerns so you must tell it. The URL option name is </span>

<span data-offset-key="7a388ef98bcf47fd8f832876af90c50d:1">`CURLOPT_URL`</span>

<span data-offset-key="7a388ef98bcf47fd8f832876af90c50d:2"> as all options are prefixed with </span>

<span data-offset-key="7a388ef98bcf47fd8f832876af90c50d:3">`CURLOPT_`</span>

<span data-offset-key="7a388ef98bcf47fd8f832876af90c50d:4"> and then the descriptive name—all using uppercase letters. An example line setting the URL to get the "</span>

</span>

<a href="http://example.com/" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="9163cbd443594ee89d98866ea7dbbddb">

<span data-offset-key="9163cbd443594ee89d98866ea7dbbddb:0">http://example.com</span>

</span>

</a>

<span data-key="5e09f99e77e843db820703d8a5406ca6">

<span data-offset-key="5e09f99e77e843db820703d8a5406ca6:0">" HTTP contents could look like:</span>

</span>

</span>    CURLcode ret = curl_easy_setopt(easy, CURLOPT_URL, "http://example.com");<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b14c34470fa14b88950232f52c414c1b">

<span data-offset-key="b14c34470fa14b88950232f52c414c1b:0">Again: this only sets the option in the handle. It will not do the actual transfer or anything. It will just tell libcurl to copy the string and if that works it returns OK.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="60fb7001c0fd4c4194837fa75b761cd6">

<span data-offset-key="60fb7001c0fd4c4194837fa75b761cd6:0">It is, of course, good form to check the return code to see that nothing went wrong.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="18a27c1807fe4a5fa49f960e60b87ee0">

<span data-offset-key="18a27c1807fe4a5fa49f960e60b87ee0:0">Setting numerical options</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c46aebb359b84027b6bf1cfd8f09ea0b">

<span data-offset-key="c46aebb359b84027b6bf1cfd8f09ea0b:0">Since curl_easy_setopt() is a vararg function where the 3rd argument can use different types depending on the situation, normal C language type conversion cannot be done. So you </span>

<span data-offset-key="c46aebb359b84027b6bf1cfd8f09ea0b:1">**must**</span>

<span data-offset-key="c46aebb359b84027b6bf1cfd8f09ea0b:2"> make sure that you truly pass a 'long' and not an 'int' if the documentation tells you so. On architectures where they are the same size, you may not get any problems but not all work like that. Similarly, for options that accept a 'curl_off_t' type, it is </span>

<span data-offset-key="c46aebb359b84027b6bf1cfd8f09ea0b:3">**crucial**</span>

<span data-offset-key="c46aebb359b84027b6bf1cfd8f09ea0b:4"> that you pass in an argument using that type and no other.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="26dcc963bfac4fe2bab5737cb1755634">

<span data-offset-key="26dcc963bfac4fe2bab5737cb1755634:0">Enforce a long:</span>

</span>

</span>    curl_easy_setopt(handle, CURLOPT_TIMEOUT, 5L); /* 5 seconds timeout */<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8b6489150a14495db26b7351dd84294d">

<span data-offset-key="8b6489150a14495db26b7351dd84294d:0">Enforce a curl_off_t:</span>

</span>

</span>    curl_off_t no_larger_than = 0x50000;curl_easy_setopt(handle, CURLOPT_MAXFILE_LARGE, no_larger_than);<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="69ba06e9039d401c8a72e85e88489ee0">

<span data-offset-key="69ba06e9039d401c8a72e85e88489ee0:0">Get handle options</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="530bd6a9e919405aa5690c76e25b0acd">

<span data-offset-key="530bd6a9e919405aa5690c76e25b0acd:0">No, there's no general method to extract the same information you previously set with </span>

<span data-offset-key="530bd6a9e919405aa5690c76e25b0acd:1">`curl_easy_setopt()`</span>

<span data-offset-key="530bd6a9e919405aa5690c76e25b0acd:2">! If you need to be able to extract the information again that you set earlier, then we encourage you to keep track of that data yourself in your application.</span>

</span>

</span>

<a href="threading.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">multi-threading</span>

<a href="options/tlsoptions.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">TLS options</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 12 months ago</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="options.html#setting-numerical-options" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Setting numerical options</span>

</span>

<a href="options.html#get-handle-options" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Get handle options</span>

</span>
