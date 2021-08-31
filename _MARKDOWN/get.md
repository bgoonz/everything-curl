<a href="get.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Get a simple HTTP page</span>

</a>

<a href="getinmem.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Get a page in memory</span>

</a>

<a href="login.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Submit a login form over HTTP</span>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Get a simple HTTP page</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="997f32fd9a404b7abf31713fb156b371">

<span data-offset-key="997f32fd9a404b7abf31713fb156b371:0">This example just fetches the HTML from a given URL and sends it to stdout. Possibly the simplest libcurl program you can write.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a26ff88067fa469698092a321d2ad00c">

<span data-offset-key="a26ff88067fa469698092a321d2ad00c:0">By replacing the URL this will of course be able to get contents over other supported protocols as well.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0206a03c1769451a8095d5bef4b18260">

<span data-offset-key="0206a03c1769451a8095d5bef4b18260:0">Getting the output sent to stdout is a default behavior and usually not what you actually want. Most applications will instead install a </span>

</span>

<a href="../callbacks/write.html" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="294e69e738e7421d939804620a64ae1e">

<span data-offset-key="294e69e738e7421d939804620a64ae1e:0">write callback</span>

</span>

</a>

<span data-key="4627b4d1f0e942d7b056e3c964d4bd83">

<span data-offset-key="4627b4d1f0e942d7b056e3c964d4bd83:0"> to have receive the data that arrives.</span>

</span>

</span>    #include <stdio.h>

#include <curl/curl.h>​int main(void){  CURL *curl;  CURLcode res;​  curl = curl_easy_init();  if(curl) {    curl_easy_setopt(curl, CURLOPT_URL, "http://example.com/");​    /* Perform the request, res will get the return code */    res = curl_easy_perform(curl);    /* Check for errors */    if(res != CURLE_OK)      fprintf(stderr, "curl_easy_perform() failed: %s\n",              curl_easy_strerror(res));​    /* always cleanup */    curl_easy_cleanup(curl);  }  return 0;}<a href="../examples.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">libcurl examples</span>

<a href="getinmem.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Get a page in memory</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>
