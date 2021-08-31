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

<a href="libcurl.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

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

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">--libcurl</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2584bd689854459783478f6201e80324">

<span data-offset-key="2584bd689854459783478f6201e80324:0">We actively encourage users to first try out the transfer they want to do with the curl command-line tool, and once it works roughly the way you want it to, you append the </span>

<span data-offset-key="2584bd689854459783478f6201e80324:1">`--libcurl [filename]`</span>

<span data-offset-key="2584bd689854459783478f6201e80324:2"> option to the command line and run it again.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e8910d79b2b347a59b5074ac091ddacf">

<span data-offset-key="e8910d79b2b347a59b5074ac091ddacf:0">The </span>

<span data-offset-key="e8910d79b2b347a59b5074ac091ddacf:1">`--libcurl`</span>

<span data-offset-key="e8910d79b2b347a59b5074ac091ddacf:2"> command-line option will create a C program in the provided file name. That C program is an application that uses libcurl to run the transfer you just had the curl command-line tool do. There are some exceptions and it is not always a 100% match, but you will find that it can serve as an excellent inspiration source for what libcurl options you want or can use and what additional arguments to provide to them.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6b3bfa2cb3374fe094edee5283e038d9">

<span data-offset-key="6b3bfa2cb3374fe094edee5283e038d9:0">If you specify the filename as a single dash, as in </span>

<span data-offset-key="6b3bfa2cb3374fe094edee5283e038d9:1">`--libcurl -`</span>

<span data-offset-key="6b3bfa2cb3374fe094edee5283e038d9:2"> you will get the program written to stdout instead of a file.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="26040a1997bc4480a10e05ce84b227b6">

<span data-offset-key="26040a1997bc4480a10e05ce84b227b6:0">As an example, we run a command to just get </span>

</span>

<a href="http://example.com/" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="b5d9840f4c3748c9a78372e1ddce4f99">

<span data-offset-key="b5d9840f4c3748c9a78372e1ddce4f99:0">http://example.com</span>

</span>

</a>

<span data-key="395b1211d1274331b6d1096b95684d24">

<span data-offset-key="395b1211d1274331b6d1096b95684d24:0">:</span>

</span>

</span> curl http://example.com --libcurl example.c<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="61d4b75943c64fd192d5392912c96c09">

<span data-offset-key="61d4b75943c64fd192d5392912c96c09:0">This creates </span>

<span data-offset-key="61d4b75943c64fd192d5392912c96c09:1">`example.c`</span>

<span data-offset-key="61d4b75943c64fd192d5392912c96c09:2"> in the current directory, looking similar to this:</span>

</span>

</span> /****\***** Sample code generated by the curl command-line tool ****\*\***** _ All curl_easy_setopt() options are documented at: _ https://curl.se/libcurl/c/curl_easy_setopt.html **********************************\*\*\*\***********************************/#include <curl/curl.h>​int main(int argc, char *argv[]){ CURLcode ret; CURL *hnd;​ hnd = curl_easy_init(); curl_easy_setopt(hnd, CURLOPT_URL, "http://example.com"); curl_easy_setopt(hnd, CURLOPT_NOPROGRESS, 1L); curl_easy_setopt(hnd, CURLOPT_USERAGENT, "curl/7.45.0"); curl_easy_setopt(hnd, CURLOPT_MAXREDIRS, 50L); curl_easy_setopt(hnd, CURLOPT_SSH_KNOWNHOSTS, "/home/daniel/.ssh/known_hosts"); curl_easy_setopt(hnd, CURLOPT_TCP_KEEPALIVE, 1L);​ /_ Here is a list of options the curl code used that cannot get generated as source easily. You may select to either not use them or implement them yourself.​ CURLOPT_WRITEDATA set to a objectpointer CURLOPT_WRITEFUNCTION set to a functionpointer CURLOPT_READDATA set to a objectpointer CURLOPT_READFUNCTION set to a functionpointer CURLOPT_SEEKDATA set to a objectpointer CURLOPT_SEEKFUNCTION set to a functionpointer CURLOPT_ERRORBUFFER set to a objectpointer CURLOPT_STDERR set to a objectpointer CURLOPT_HEADERFUNCTION set to a functionpointer CURLOPT_HEADERDATA set to a objectpointer​ _/​ ret = curl_easy_perform(hnd);​ curl_easy_cleanup(hnd); hnd = NULL;​ return (int)ret;}/\***\* End of sample code \*\***/<a href="api.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">API compatibility</span>

<a href="headers.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Header files</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 8 months ago</span>
