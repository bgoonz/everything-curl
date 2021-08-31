<a href="get.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Get a simple HTTP page</span>

</a>

<a href="getinmem.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Get a page in memory</span>

</a>

<a href="login.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Submit a login form over HTTP</span>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Submit a login form over HTTP</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c95edc056a754b7fbc3e23a62f935163">

<span data-offset-key="c95edc056a754b7fbc3e23a62f935163:0">A login submission over HTTP is usually a matter of figuring out exactly what data to submit in a POST and to which target URL to send it.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e03ac3dc9539489d822e16034e0bdea9">

<span data-offset-key="e03ac3dc9539489d822e16034e0bdea9:0">Once logged in, the target URL can be fetched if the proper cookies are used. As many login-systems work with HTTP redirects, we ask libcurl to follow such if they arrive.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="77fe6f9213de464c91d69dded99c65c7">

<span data-offset-key="77fe6f9213de464c91d69dded99c65c7:0">Some login forms will make it more complicated and require that you got cookies from the page showing the login form etc, so if you need that you may want to extend this code a little bit.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6b366477b663408d883b870e8e088373">

<span data-offset-key="6b366477b663408d883b870e8e088373:0">By passing in a non-existing cookie file, this example will enable the cookie parser so incoming cookies will be stored when the response from the login response arrives and then the subsequent request for the resource will use those and prove to the server that we are in fact correctly logged in.</span>

</span>

</span> #include <stdio.h>

#include <string.h>

#include <curl/curl.h>​int main(void){ CURL *curl; CURLcode res;​ static const char *postthis = "user=daniel&password=monkey123";​ curl = curl_easy_init(); if(curl) { curl_easy_setopt(curl, CURLOPT_URL, "https://example.com/login.cgi"); curl_easy_setopt(curl, CURLOPT_POSTFIELDS, postthis); curl_easy_setopt(curl, CURLOPT_FOLLOWLOCATION, 1L); /_ redirects! _/ curl_easy_setopt(curl, CURLOPT_COOKIEFILE, ""); /_ no file _/ res = curl_easy_perform(curl); /_ Check for errors _/ if(res != CURLE_OK) fprintf(stderr, "curl_easy_perform() failed: %s\n", curl_easy_strerror(res)); else { /\* _ After the login POST, we have received the new cookies. Switch _ over to a GET and ask for the login-protected URL. _/ curl_easy_setopt(curl, CURLOPT_URL, "https://example.com/file"); curl_easy_setopt(curl, CURLOPT_HTTPGET, 1L); /_ no more POST _/ res = curl_easy_perform(curl); /_ Check for errors _/ if(res != CURLE_OK) fprintf(stderr, "second curl_easy_perform() failed: %s\n", curl_easy_strerror(res)); } /_ always cleanup \*/ curl_easy_cleanup(curl); } return 0;}<a href="getinmem.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Get a page in memory</span>

<a href="../cplusplus.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">for C++ programmers</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>
