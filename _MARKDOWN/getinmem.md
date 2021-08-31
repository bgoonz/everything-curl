<a href="get.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Get a simple HTTP page</span>

</a>

<a href="getinmem.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Get a page in memory</span>

</a>

<a href="login.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Submit a login form over HTTP</span>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Get a page in memory</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="161b751f1b3b4a11bb32a20514b2d18a">

<span data-offset-key="161b751f1b3b4a11bb32a20514b2d18a:0">This example is a variation of the former that instead of sending the received data to stdout (which often is not what you want), this example instead stores the incoming data in a memory buffer that is enlarged as the incoming data grows.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9f8ae688c9b443cab1e83f12aeface3b">

<span data-offset-key="9f8ae688c9b443cab1e83f12aeface3b:0">It accomplishes this by using a </span>

</span>

<a href="../callbacks/write.html" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="eb84c32a3a4a4ae8a55e5e4404682cad">

<span data-offset-key="eb84c32a3a4a4ae8a55e5e4404682cad:0">write callback</span>

</span>

</a>

<span data-key="aea49d3ca6d64503a1e4db73c42fe97e">

<span data-offset-key="aea49d3ca6d64503a1e4db73c42fe97e:0"> to receive the data.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="472e3e176fcc438f830a8fdb40cfbbd4">

<span data-offset-key="472e3e176fcc438f830a8fdb40cfbbd4:0">This example uses a fixed URL string with a set URL scheme, but you can of course change this to use any other supported protocol and then get a resource from that instead.</span>

</span>

</span> #include <stdio.h>

#include <stdlib.h>

#include <string.h>​#include <curl/curl.h>​struct MemoryStruct { char *memory; size_t size;};​static size_tWriteMemoryCallback(void *contents, size_t size, size_t nmemb, void _userp){ size_t realsize = size _ nmemb; struct MemoryStruct _mem = (struct MemoryStruct _)userp;​ mem->memory = realloc(mem->memory, mem->size + realsize + 1); if(mem->memory == NULL) { /_ out of memory _/ printf("not enough memory (realloc returned NULL)\n"); return 0; }​ memcpy(&(mem->memory[mem->size]), contents, realsize); mem->size += realsize; mem->memory[mem->size] = 0;​ return realsize;}​int main(void){ CURL _curl_handle; CURLcode res;​ struct MemoryStruct chunk;​ chunk.memory = malloc(1); /_ will be grown as needed by the realloc above _/ chunk.size = 0; /_ no data at this point _/​ curl_global_init(CURL_GLOBAL_ALL);​ /_ init the curl session _/ curl_handle = curl_easy_init();​ /_ specify URL to get _/ curl_easy_setopt(curl_handle, CURLOPT_URL, "https://www.example.com/");​ /_ send all data to this function _/ curl_easy_setopt(curl_handle, CURLOPT_WRITEFUNCTION, WriteMemoryCallback);​ /_ we pass our 'chunk' struct to the callback function _/ curl_easy_setopt(curl_handle, CURLOPT_WRITEDATA, (void _)&chunk);​ /_ some servers do not like requests that are made without a user-agent field, so we provide one _/ curl_easy_setopt(curl_handle, CURLOPT_USERAGENT, "libcurl-agent/1.0");​ /_ get it! _/ res = curl_easy_perform(curl_handle);​ /_ check for errors _/ if(res != CURLE_OK) { fprintf(stderr, "curl_easy_perform() failed: %s\n", curl_easy_strerror(res)); } else { /\* _ Now, our chunk.memory points to a memory block that is chunk.size _ bytes big and contains the remote file. \* _ Do something nice with it! _/​ printf("%lu bytes retrieved\n", (long)chunk.size); }​ /_ cleanup curl stuff _/ curl_easy_cleanup(curl_handle);​ free(chunk.memory);​ /_ we are done with libcurl, so clean it up _/ curl_global_cleanup();​ return 0;}<a href="get.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Get a simple HTTP page</span>

<a href="login.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Submit a login form over HTTP</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>
