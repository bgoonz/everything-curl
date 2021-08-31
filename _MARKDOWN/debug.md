<a href="write.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Write data</span>

</a>

<a href="debug.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Debug</span>

</a>

<a href="sshkey.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">SSH key</span>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Debug</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="5f25d5856b1e4ae6aa8276c95d8c18f7">

<span data-offset-key="5f25d5856b1e4ae6aa8276c95d8c18f7:0">The debug callback is set with </span>

<span data-offset-key="5f25d5856b1e4ae6aa8276c95d8c18f7:1">`CURLOPT_DEBUGFUNCTION`</span>

<span data-offset-key="5f25d5856b1e4ae6aa8276c95d8c18f7:2">:</span>

</span>

</span> curl_easy_setopt(handle, CURLOPT_DEBUGFUNCTION, debug_callback);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="cf6ce9120cbd4615be33706e76cb28cf">

<span data-offset-key="cf6ce9120cbd4615be33706e76cb28cf:0">The </span>

<span data-offset-key="cf6ce9120cbd4615be33706e76cb28cf:1">`debug_callback`</span>

<span data-offset-key="cf6ce9120cbd4615be33706e76cb28cf:2"> function must match this prototype:</span>

</span>

</span> int debug_callback(CURL *handle, curl_infotype type, char *data, size_t size, void \*userdata);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="1c2f7464bfe5484797bc228e8c3baf83">

<span data-offset-key="1c2f7464bfe5484797bc228e8c3baf83:0">This callback function replaces the default verbose output function in the library and will get called for all debug and trace messages to aid applications to understand what's going on. The </span>

<span data-offset-key="1c2f7464bfe5484797bc228e8c3baf83:1">_type_</span>

<span data-offset-key="1c2f7464bfe5484797bc228e8c3baf83:2"> argument explains what sort of data that is provided: header, data or SSL data and in which direction it flows.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="1765dcafe99847d7a6aeb1ab9b95f6d2">

<span data-offset-key="1765dcafe99847d7a6aeb1ab9b95f6d2:0">A common use for this callback is to get a full trace of all data that libcurl sends and receives. The data sent to this callback is always the unencrypted version, even when, for example, HTTPS or other encrypted protocols are used.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7a3df8ec136e45c3be9f0e6f7ccdb862">

<span data-offset-key="7a3df8ec136e45c3be9f0e6f7ccdb862:0">This callback must return zero or cause the transfer to stop with an error code.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="fca958c9ea414c8db6bc98732846b839">

<span data-offset-key="fca958c9ea414c8db6bc98732846b839:0">The user pointer passed in to the callback in the </span>

<span data-offset-key="fca958c9ea414c8db6bc98732846b839:1">_userdata_</span>

<span data-offset-key="fca958c9ea414c8db6bc98732846b839:2"> argument is set with </span>

<span data-offset-key="fca958c9ea414c8db6bc98732846b839:3">`CURLOPT_DEBUGDATA`</span>

<span data-offset-key="fca958c9ea414c8db6bc98732846b839:4">:</span>

</span>

</span> curl_easy_setopt(handle, CURLOPT_DEBUGDATA, custom_pointer);<a href="header.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Header data</span>

<a href="sockopt.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">sockopt</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>
