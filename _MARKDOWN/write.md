<a href="write.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Write data</span>

</a>

<a href="sshkey.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">SSH key</span>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Write data</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ce358962aa5a43408e280a73aca0c21b">

<span data-offset-key="ce358962aa5a43408e280a73aca0c21b:0">The write callback is set with </span>

<span data-offset-key="ce358962aa5a43408e280a73aca0c21b:1">`CURLOPT_WRITEFUNCTION`</span>

<span data-offset-key="ce358962aa5a43408e280a73aca0c21b:2">:</span>

</span>

</span> curl_easy_setopt(handle, CURLOPT_WRITEFUNCTION, write_callback);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="687bb2043543411683e6bc5163a7746f">

<span data-offset-key="687bb2043543411683e6bc5163a7746f:0">The </span>

<span data-offset-key="687bb2043543411683e6bc5163a7746f:1">`write_callback`</span>

<span data-offset-key="687bb2043543411683e6bc5163a7746f:2"> function must match this prototype:</span>

</span>

</span> size_t write_callback(char *ptr, size_t size, size_t nmemb, void *userdata);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c719dced6322404c95083cfe8dade036">

<span data-offset-key="c719dced6322404c95083cfe8dade036:0">This callback function gets called by libcurl as soon as there is data received that needs to be saved. </span>

<span data-offset-key="c719dced6322404c95083cfe8dade036:1">_ptr_</span>

<span data-offset-key="c719dced6322404c95083cfe8dade036:2"> points to the delivered data, and the size of that data is </span>

<span data-offset-key="c719dced6322404c95083cfe8dade036:3">_size_</span>

<span data-offset-key="c719dced6322404c95083cfe8dade036:4"> multiplied with </span>

<span data-offset-key="c719dced6322404c95083cfe8dade036:5">_nmemb_</span>

<span data-offset-key="c719dced6322404c95083cfe8dade036:6">.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="45cc59b911fb4788bbd90ff7dd98b740">

<span data-offset-key="45cc59b911fb4788bbd90ff7dd98b740:0">If this callback is not set, libcurl instead uses 'fwrite' by default.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e62a3561877c4fbe84034f2ad5763e11">

<span data-offset-key="e62a3561877c4fbe84034f2ad5763e11:0">The write callback will be passed as much data as possible in all invokes, but it must not make any assumptions. It may be one byte, it may be thousands. The maximum amount of body data that will be passed to the write callback is defined in the curl.h header file: </span>

<span data-offset-key="e62a3561877c4fbe84034f2ad5763e11:1">`CURL_MAX_WRITE_SIZE`</span>

<span data-offset-key="e62a3561877c4fbe84034f2ad5763e11:2"> (the usual default is 16KB). If </span>

<span data-offset-key="e62a3561877c4fbe84034f2ad5763e11:3">`CURLOPT_HEADER`</span>

<span data-offset-key="e62a3561877c4fbe84034f2ad5763e11:4"> is enabled for this transfer, which makes header data get passed to the write callback, you can get up to </span>

<span data-offset-key="e62a3561877c4fbe84034f2ad5763e11:5">`CURL_MAX_HTTP_HEADER`</span>

<span data-offset-key="e62a3561877c4fbe84034f2ad5763e11:6"> bytes of header data passed into it. This usually means 100KB.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="96b3c3f8410445ef8738a7699bed94bb">

<span data-offset-key="96b3c3f8410445ef8738a7699bed94bb:0">This function may be called with zero bytes data if the transferred file is empty.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="66c2e90274324d93b388b909625651d1">

<span data-offset-key="66c2e90274324d93b388b909625651d1:0">The data passed to this function will not be zero terminated! You cannot, for example, use printf's </span>

<span data-offset-key="66c2e90274324d93b388b909625651d1:1">`%s`</span>

<span data-offset-key="66c2e90274324d93b388b909625651d1:2"> operator to display the contents nor strcpy to copy it.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="62f4ff7c799f48289e3ce9494de2612e">

<span data-offset-key="62f4ff7c799f48289e3ce9494de2612e:0">This callback should return the number of bytes actually taken care of. If that number differs from the number passed to your callback function, it will signal an error condition to the library. This will cause the transfer to get aborted and the libcurl function used will return </span>

<span data-offset-key="62f4ff7c799f48289e3ce9494de2612e:1">`CURLE_WRITE_ERROR`</span>

<span data-offset-key="62f4ff7c799f48289e3ce9494de2612e:2">.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9c973fd2f19b4c188601f16f3bd7d6bb">

<span data-offset-key="9c973fd2f19b4c188601f16f3bd7d6bb:0">The user pointer passed in to the callback in the </span>

<span data-offset-key="9c973fd2f19b4c188601f16f3bd7d6bb:1">_userdata_</span>

<span data-offset-key="9c973fd2f19b4c188601f16f3bd7d6bb:2"> argument is set with </span>

<span data-offset-key="9c973fd2f19b4c188601f16f3bd7d6bb:3">`CURLOPT_WRITEDATA`</span>

<span data-offset-key="9c973fd2f19b4c188601f16f3bd7d6bb:4">:</span>

</span>

</span> curl_easy_setopt(handle, CURLOPT_WRITEDATA, custom_pointer);<a href="../callbacks.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Callbacks</span>

<a href="read.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Read data</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>
