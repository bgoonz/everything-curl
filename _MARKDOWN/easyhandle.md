<a href="easyhandle.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

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

<a href="curlcode.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">CURLcode return codes</span>

</a>

<a href="verbose.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Verbose operations</span>

</a>

<a href="cplusplus.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">for C++ programmers</span>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Easy handle</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4e69f1a70e124974b1323e351524e505">

<span data-offset-key="4e69f1a70e124974b1323e351524e505:0">The fundamentals you need to learn with libcurl:</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0981acf7009248afaf7b661592113dbd">

<span data-offset-key="0981acf7009248afaf7b661592113dbd:0">First you create an "easy handle", which is your handle to a transfer, really:</span>

</span>

</span> CURL \*easy_handle = curl_easy_init();<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a25aac2bb8e64ad3b5e7429de0009a27">

<span data-offset-key="a25aac2bb8e64ad3b5e7429de0009a27:0">You then set options in that handle to control the upcoming transfer. This example sets the URL:</span>

</span>

</span> /_ set URL to operate on _/res = curl_easy_setopt(easy_handle, CURLOPT_URL, "http://example.com/");<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2fe99edec715435a8e141b0c17e081cf">

<span data-offset-key="2fe99edec715435a8e141b0c17e081cf:0">If </span>

<span data-offset-key="2fe99edec715435a8e141b0c17e081cf:1">`curl_easy_setopt()`</span>

<span data-offset-key="2fe99edec715435a8e141b0c17e081cf:2"> returns </span>

<span data-offset-key="2fe99edec715435a8e141b0c17e081cf:3">`CURLE_OK`</span>

<span data-offset-key="2fe99edec715435a8e141b0c17e081cf:4">, we know it stored the option fine.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="eeccaa0fe7fb4c4cb7b03a2feb324f91">

<span data-offset-key="eeccaa0fe7fb4c4cb7b03a2feb324f91:0">Creating the easy handle and setting options on it does not make any transfer happen, and usually do not even make much more happen other than libcurl storing your wish to be used later when the transfer actually occurs. Lots of syntax checking and validation of the input may also be postponed, so just because </span>

<span data-offset-key="eeccaa0fe7fb4c4cb7b03a2feb324f91:1">`curl_easy_setopt`</span>

<span data-offset-key="eeccaa0fe7fb4c4cb7b03a2feb324f91:2"> did not complain, it does not mean that the input was correct and valid; you may get an error returned later.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="93ff4db06d124818add036bdded33090">

<span data-offset-key="93ff4db06d124818add036bdded33090:0">Read more on </span>

</span>

<a href="https://github.com/bagder/everything-curl/tree/af5b2aacc2c06b35e7cbe5ea5f6f6ae11217b931/libcurl/libcurl-options.md" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="f678f152f4db4402b084f5e093e4e8da">

<span data-offset-key="f678f152f4db4402b084f5e093e4e8da:0">easy options</span>

</span>

</a>

<span data-key="7c732493351e486abaaabe769745d504">

<span data-offset-key="7c732493351e486abaaabe769745d504:0"> in its separate section.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f3d7534ca5b642e0ae99453663586d04">

<span data-offset-key="f3d7534ca5b642e0ae99453663586d04:0">When you are done setting options to your easy handle, you can fire off the actual transfer.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="425ae0634baf437188e43f02238d9c85">

<span data-offset-key="425ae0634baf437188e43f02238d9c85:0">The actual performing of the transfer can be done using different methods and function calls, depending on what kind of behavior you want in your application and how libcurl is best integrated into your architecture. Those are further described later in this chapter.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="d4829c453e4f463d8712be7a03618957">

<span data-offset-key="d4829c453e4f463d8712be7a03618957:0">While the transfer is ongoing, libcurl calls your specified functions—known as </span>

</span>

<a href="https://github.com/bagder/everything-curl/tree/af5b2aacc2c06b35e7cbe5ea5f6f6ae11217b931/libcurl/libcurl-callbacks.md%5D" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="40c4674141584e2cb9c0f80abbda68b8">

<span data-offset-key="40c4674141584e2cb9c0f80abbda68b8:0">

<em>callbacks</em>

</span>

</span>

</a>

<span data-key="9b244133e3a743ffb98ed43da9132e8f">

<span data-offset-key="9b244133e3a743ffb98ed43da9132e8f:0"> — to deliver data, to read data or to do a wide variety of things.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4012b8de951244faa8261b34d21eebad">

<span data-offset-key="4012b8de951244faa8261b34d21eebad:0">After the transfer has completed, you can figure out if it succeeded or not and you can extract statistics and other information that libcurl gathered during the transfer from the easy handle. See </span>

</span>

<a href="https://github.com/bagder/everything-curl/tree/af5b2aacc2c06b35e7cbe5ea5f6f6ae11217b931/libcurl/libcurl-getinfo.md" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="dd039b8039ee4a9aa5a5823cfd3f19a9">

<span data-offset-key="dd039b8039ee4a9aa5a5823cfd3f19a9:0">Post transfer information</span>

</span>

</a>

<span data-key="8f958b226ee04f10a2758a7a4d7c6e37">

<span data-offset-key="8f958b226ee04f10a2758a7a4d7c6e37:0">.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="7fc3655fd66d4e07b13fe3b0f90a220c">

<span data-offset-key="7fc3655fd66d4e07b13fe3b0f90a220c:0">Reuse!</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="d8339476ea3e43cc9697ce844ff1035c">

<span data-offset-key="d8339476ea3e43cc9697ce844ff1035c:0">Easy handles are meant and designed to be reused. When you have done a single transfer with the easy handle, you can immediately use it again for your next transfer. There are lots of gains to be had by this.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0ff8ee333ae34e3898e65db52dc41678">

<span data-offset-key="0ff8ee333ae34e3898e65db52dc41678:0">All options are "sticky". They remain set in the handle until you change them again, or call </span>

<span data-offset-key="0ff8ee333ae34e3898e65db52dc41678:1">`curl_easy_reset()`</span>

<span data-offset-key="0ff8ee333ae34e3898e65db52dc41678:2"> on the handle. If you make a second transfer with the same handle, the same options are used.</span>

</span>

</span>

<a href="../libcurl.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">libcurl basics</span>

<a href="drive.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Drive transfers</span>
