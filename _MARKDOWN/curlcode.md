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

<a href="curlcode.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">CURLcode return codes</span>

</a>

<a href="verbose.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Verbose operations</span>

</a>

<a href="cplusplus.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">for C++ programmers</span>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">CURLcode return codes</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="548514f9d24946b397f5cb23f5f716de">

<span data-offset-key="548514f9d24946b397f5cb23f5f716de:0">Many libcurl functions return a CURLcode. That's a special libcurl typedefed variable for error codes. It returns </span>

<span data-offset-key="548514f9d24946b397f5cb23f5f716de:1">`CURLE_OK`</span>

<span data-offset-key="548514f9d24946b397f5cb23f5f716de:2"> (which has the value zero) if everything is fine and dandy and it returns a non-zero number if a problem was detected. There are almost one hundred </span>

<span data-offset-key="548514f9d24946b397f5cb23f5f716de:3">`CURLcode`</span>

<span data-offset-key="548514f9d24946b397f5cb23f5f716de:4"> errors in use, and you can find them all in the </span>

<span data-offset-key="548514f9d24946b397f5cb23f5f716de:5">`curl/curl.h`</span>

<span data-offset-key="548514f9d24946b397f5cb23f5f716de:6"> header file and documented in the libcurl-errors man page.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7da0b9a3a23c40419d9800278b88c9b9">

<span data-offset-key="7da0b9a3a23c40419d9800278b88c9b9:0">You can convert a CURLcode into a human readable string with the </span>

<span data-offset-key="7da0b9a3a23c40419d9800278b88c9b9:1">`curl_easy_strerror()`</span>

<span data-offset-key="7da0b9a3a23c40419d9800278b88c9b9:2"> function—but be aware that these errors are rarely phrased in a way that is suitable for anyone to expose in a UI or to an end user:</span>

</span>

</span> const char \*str = curl_easy_strerror( error );printf("libcurl said %s\n", str);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="47995388febb4e5abc4dc1835e0fa82f">

<span data-offset-key="47995388febb4e5abc4dc1835e0fa82f:0">Another way to get a slightly better error text in case of errors is to set the </span>

<span data-offset-key="47995388febb4e5abc4dc1835e0fa82f:1">`CURLOPT_ERRORBUFFER`</span>

<span data-offset-key="47995388febb4e5abc4dc1835e0fa82f:2"> option to point out a buffer in your program and then libcurl will store a related error message there before it returns an error:</span>

</span>

</span> char error[CURL_ERROR_SIZE]; /_ needs to be at least this big _/CURLcode ret = curl_easy_setopt(handle, CURLOPT_ERRORBUFFER, error);<a href="options/tlsoptions.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">TLS options</span>

<a href="verbose.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Verbose operations</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 1 month ago</span>
