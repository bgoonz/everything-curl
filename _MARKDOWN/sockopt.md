<a href="write.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Write data</span>
</a>
<a href="sockopt.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">sockopt</span>
</a>
<a href="sshkey.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">SSH key</span>
</a># <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">sockopt</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="69203f0c54d14c82b71ddfdebcfe5d55">
<span data-offset-key="69203f0c54d14c82b71ddfdebcfe5d55:0">The sockopt callback is set with </span>
<span data-offset-key="69203f0c54d14c82b71ddfdebcfe5d55:1">`CURLOPT_SOCKOPTFUNCTION`</span>
<span data-offset-key="69203f0c54d14c82b71ddfdebcfe5d55:2">:</span>
</span>
</span>    curl_easy_setopt(handle, CURLOPT_SOCKOPTFUNCTION, sockopt_callback);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="82df76fd020d40b28fee70568f4bc0b8">
<span data-offset-key="82df76fd020d40b28fee70568f4bc0b8:0">The </span>
<span data-offset-key="82df76fd020d40b28fee70568f4bc0b8:1">`sockopt_callback`</span>
<span data-offset-key="82df76fd020d40b28fee70568f4bc0b8:2"> function must match this prototype:</span>
</span>
</span>    int sockopt_callback(void *clientp,                     curl_socket_t curlfd,                     curlsocktype purpose);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="19c801ef27014fc89b774199bab2a1f6">
<span data-offset-key="19c801ef27014fc89b774199bab2a1f6:0">This callback function gets called by libcurl when a new socket has been created but before the connect call, to allow applications to change specific socket options.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="70de59fe20864ab6935791e83536ca88">
<span data-offset-key="70de59fe20864ab6935791e83536ca88:0">The </span>
<span data-offset-key="70de59fe20864ab6935791e83536ca88:1">**clientp**</span>
<span data-offset-key="70de59fe20864ab6935791e83536ca88:2"> pointer points to the private data set with </span>
<span data-offset-key="70de59fe20864ab6935791e83536ca88:3">`CURLOPT_SOCKOPTDATA`</span>
<span data-offset-key="70de59fe20864ab6935791e83536ca88:4">:</span>
</span>
</span>    curl_easy_setopt(handle, CURLOPT_SOCKOPTDATA, custom_pointer);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="8720eb764498493a91a49c0950bc246b">
<span data-offset-key="8720eb764498493a91a49c0950bc246b:0">This callback should return:</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="962ed33690514980bd6d3430450906a0">
<span data-offset-key="962ed33690514980bd6d3430450906a0:0">CURL_SOCKOPT_OK on success</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="b925e0832a4845a88cdeae453e20146b">
<span data-offset-key="b925e0832a4845a88cdeae453e20146b:0">CURL_SOCKOPT_ERROR to signal an unrecoverable error to libcurl</span>
</span>
</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="c7dfa07c22264aa08c2c9b891ceaf561">
<span data-offset-key="c7dfa07c22264aa08c2c9b891ceaf561:0">CURL_SOCKOPT_ALREADY_CONNECTED to signal success but also that the socket is</span>
</span>
</span>  <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="9ef31a5e609540be9d8eb792d4f41a46">
<span data-offset-key="9ef31a5e609540be9d8eb792d4f41a46:0">in fact already connected to the destination</span>
</span>
</span>
<a href="debug.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">
</a>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Debug</span>
<a href="sslcontext.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">
</a>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">SSL context</span>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>
