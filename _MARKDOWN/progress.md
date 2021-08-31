<a href="write.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Write data</span>

</a>

<a href="progress.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Progress information</span>

</a>

<a href="sshkey.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">SSH key</span>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Progress information</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="891ac1259cce454cbad8281f0a2582c2">

<span data-offset-key="891ac1259cce454cbad8281f0a2582c2:0">The progress callback is what gets called regularly and repeatedly for each transfer during the entire lifetime of the transfer. The old callback was set with </span>

<span data-offset-key="891ac1259cce454cbad8281f0a2582c2:1">`CURLOPT_PROGRESSFUNCTION`</span>

<span data-offset-key="891ac1259cce454cbad8281f0a2582c2:2"> but the modern and preferred callback is set with </span>

<span data-offset-key="891ac1259cce454cbad8281f0a2582c2:3">`CURLOPT_XFERINFOFUNCTION`</span>

<span data-offset-key="891ac1259cce454cbad8281f0a2582c2:4">:</span>

</span>

</span> curl_easy_setopt(handle, CURLOPT_XFERINFOFUNCTION, xfer_callback);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="390be1484615413ebf4a9b3758aea678">

<span data-offset-key="390be1484615413ebf4a9b3758aea678:0">The </span>

<span data-offset-key="390be1484615413ebf4a9b3758aea678:1">`xfer_callback`</span>

<span data-offset-key="390be1484615413ebf4a9b3758aea678:2"> function must match this prototype:</span>

</span>

</span> int xfer_callback(void \*clientp, curl_off_t dltotal, curl_off_t dlnow, curl_off_t ultotal, curl_off_t ulnow);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b64dd0e55d8d48008d7de27a55c2e8fc">

<span data-offset-key="b64dd0e55d8d48008d7de27a55c2e8fc:0">If this option is set and </span>

<span data-offset-key="b64dd0e55d8d48008d7de27a55c2e8fc:1">`CURLOPT_NOPROGRESS`</span>

<span data-offset-key="b64dd0e55d8d48008d7de27a55c2e8fc:2"> is set to 0 (zero), this callback function gets called by libcurl with a frequent interval. While data is being transferred it will be called frequently, and during slow periods like when nothing is being transferred it can slow down to about one call per second.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0c796b566e934c64bf880f9bff229952">

<span data-offset-key="0c796b566e934c64bf880f9bff229952:0">The </span>

<span data-offset-key="0c796b566e934c64bf880f9bff229952:1">**clientp**</span>

<span data-offset-key="0c796b566e934c64bf880f9bff229952:2"> pointer points to the private data set with </span>

<span data-offset-key="0c796b566e934c64bf880f9bff229952:3">`CURLOPT_XFERINFODATA`</span>

<span data-offset-key="0c796b566e934c64bf880f9bff229952:4">:</span>

</span>

</span> curl_easy_setopt(handle, CURLOPT_XFERINFODATA, custom_pointer);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ae87ad8a6352444da68873b3a222bd65">

<span data-offset-key="ae87ad8a6352444da68873b3a222bd65:0">The callback gets told how much data libcurl will transfer and has transferred, in number of bytes:</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="77f6e0eae0214c7aa2db642db224c24b">

<span data-offset-key="77f6e0eae0214c7aa2db642db224c24b:0">**dltotal**</span>

<span data-offset-key="77f6e0eae0214c7aa2db642db224c24b:1"> is the total number of bytes libcurl expects to download in</span>

</span>

</span> <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="23358a6c9c274d149d719830afe99648">

<span data-offset-key="23358a6c9c274d149d719830afe99648:0">this transfer.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="039cb5d17ecd45f7a5db3f1c93846bac">

<span data-offset-key="039cb5d17ecd45f7a5db3f1c93846bac:0">**dlnow**</span>

<span data-offset-key="039cb5d17ecd45f7a5db3f1c93846bac:1"> is the number of bytes downloaded so far.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="66cf3dbe80e34809b2a91d0b25fc7da5">

<span data-offset-key="66cf3dbe80e34809b2a91d0b25fc7da5:0">**ultotal**</span>

<span data-offset-key="66cf3dbe80e34809b2a91d0b25fc7da5:1"> is the total number of bytes libcurl expects to upload in this</span>

</span>

</span> <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="19ff25a41847493c992a0ccbb9eb6a29">

<span data-offset-key="19ff25a41847493c992a0ccbb9eb6a29:0">transfer.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="03d6908801954669a71295727281cb9d">

<span data-offset-key="03d6908801954669a71295727281cb9d:0">**ulnow**</span>

<span data-offset-key="03d6908801954669a71295727281cb9d:1"> is the number of bytes uploaded so far.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="720cd647058547c2842c6e1082f8e30b">

<span data-offset-key="720cd647058547c2842c6e1082f8e30b:0">Unknown/unused argument values passed to the callback will be set to zero (like if you only download data, the upload size will remain 0). Many times the callback will be called one or more times first, before it knows the data sizes, so a program must be made to handle that.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="03cf5682f87149ddac5bb01ef97ca369">

<span data-offset-key="03cf5682f87149ddac5bb01ef97ca369:0">Returning a non-zero value from this callback will cause libcurl to abort the transfer and return </span>

<span data-offset-key="03cf5682f87149ddac5bb01ef97ca369:1">`CURLE_ABORTED_BY_CALLBACK`</span>

<span data-offset-key="03cf5682f87149ddac5bb01ef97ca369:2">.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8757ca54c5c141628dc46ac2a1382955">

<span data-offset-key="8757ca54c5c141628dc46ac2a1382955:0">If you transfer data with the multi interface, this function will not be called during periods of idleness unless you call the appropriate libcurl function that performs transfers.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="3c9af51210754b129789d9cb5b4a909e">

<span data-offset-key="3c9af51210754b129789d9cb5b4a909e:0">(The deprecated callback </span>

<span data-offset-key="3c9af51210754b129789d9cb5b4a909e:1">`CURLOPT_PROGRESSFUNCTION`</span>

<span data-offset-key="3c9af51210754b129789d9cb5b4a909e:2"> worked identically but instead of taking arguments of type </span>

<span data-offset-key="3c9af51210754b129789d9cb5b4a909e:3">`curl_off_t`</span>

<span data-offset-key="3c9af51210754b129789d9cb5b4a909e:4">, it used </span>

<span data-offset-key="3c9af51210754b129789d9cb5b4a909e:5">`double`</span>

<span data-offset-key="3c9af51210754b129789d9cb5b4a909e:6">.)</span>

</span>

</span>

<a href="read.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Read data</span>

<a href="header.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Header data</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>
