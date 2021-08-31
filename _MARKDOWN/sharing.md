h<a href="easyhandle.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

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

<a href="sharing.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

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

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Share data between handles</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6f0cb712c47f43a68a105b8e637223ae">

<span data-offset-key="6f0cb712c47f43a68a105b8e637223ae:0">Sometimes applications need to share data between transfers. All easy handles added to the same multi handle automatically get a lot of sharing done between the handles in that same multi handle, but sometimes that's not exactly what you want.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="8b676df61e364cb9b0c9ce472aeea96e">

<span data-offset-key="8b676df61e364cb9b0c9ce472aeea96e:0">Multi handle</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c9f33bc2eeda4da1b9e86982a007116d">

<span data-offset-key="c9f33bc2eeda4da1b9e86982a007116d:0">All easy handles added to the same multi handle automatically share </span>

</span>

<a href="https://github.com/bagder/everything-curl/tree/cd7d117859fa30c1ada4ad46210311d2e8295e54/libcurl-connectionreuse/README.md" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="c0a87cd0b5a54ea9bfbf04813a0f4421">

<span data-offset-key="c0a87cd0b5a54ea9bfbf04813a0f4421:0">connection cache</span>

</span>

</a>

<span data-key="0d1a4528830f43f3a73db02d1e83c366">

<span data-offset-key="0d1a4528830f43f3a73db02d1e83c366:0"> and </span>

</span>

<a href="names.html" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="dc66a1d7f3ff493099c5656b89885435">

<span data-offset-key="dc66a1d7f3ff493099c5656b89885435:0">dns cache</span>

</span>

</a>

<span data-key="e511852715a340e4b049f238395a2462">

<span data-offset-key="e511852715a340e4b049f238395a2462:0">.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="efbb6255586e453bb793c1353511b088">

<span data-offset-key="efbb6255586e453bb793c1353511b088:0">Sharing between easy handles</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4a44bd32a0734f95b3d67a04f8fd0a29">

<span data-offset-key="4a44bd32a0734f95b3d67a04f8fd0a29:0">libcurl has a generic "sharing interface", where the application creates a "share object" that then holds data that can be shared by any number of easy handles. The data is then stored and read from the shared object instead of kept within the handles that are sharing it.</span>

</span>

</span> CURLSH \*share = curl_share_init();<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="69fe2f4931b04c29978547de18b9e283">

<span data-offset-key="69fe2f4931b04c29978547de18b9e283:0">The shared object can be set to share all or any of cookies, connection cache, dns cache and SSL session id cache.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="68f88aca7d1c48faaba41351c72739a6">

<span data-offset-key="68f88aca7d1c48faaba41351c72739a6:0">For example, setting up the share to hold cookies and dns cache:</span>

</span>

</span> curl_share_setopt(share, CURLSHOPT_SHARE, CURL_LOCK_DATA_COOKIE);curl_share_setopt(share, CURLSHOPT_SHARE, CURL_LOCK_DATA_DNS);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="1f0158c185a94645bed8bd87bc4f92d7">

<span data-offset-key="1f0158c185a94645bed8bd87bc4f92d7:0">You then set up the corresponding transfer to use this share object:</span>

</span>

</span> curl_easy_setopt(curl, CURLOPT_SHARE, share);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="5c8fa428b79d462a9dc78efd4ace6ad7">

<span data-offset-key="5c8fa428b79d462a9dc78efd4ace6ad7:0">Transfers done with this </span>

<span data-offset-key="5c8fa428b79d462a9dc78efd4ace6ad7:1">`curl`</span>

<span data-offset-key="5c8fa428b79d462a9dc78efd4ace6ad7:2"> handle will thus use and store its cookie and dns information in the </span>

<span data-offset-key="5c8fa428b79d462a9dc78efd4ace6ad7:3">`share`</span>

<span data-offset-key="5c8fa428b79d462a9dc78efd4ace6ad7:4"> handle. You can set several easy handles to share the same share object.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="6976962d49f540eab3b49f83d9752381">

<span data-offset-key="6976962d49f540eab3b49f83d9752381:0">What to share</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="44fb1fe802994f49986028323a38deb3">

<span data-offset-key="44fb1fe802994f49986028323a38deb3:0">`CURL_LOCK_DATA_COOKIE`</span>

<span data-offset-key="44fb1fe802994f49986028323a38deb3:1"> - set this bit to share cookie jar. Note that each easy handle still needs to get its cookie "engine" started properly to start using cookies.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="48656812348f413a87e96878ba9bfb89">

<span data-offset-key="48656812348f413a87e96878ba9bfb89:0">`CURL_LOCK_DATA_DNS`</span>

<span data-offset-key="48656812348f413a87e96878ba9bfb89:1"> - the DNS cache is where libcurl stores addresses for resolved host names for a while to make subsequent lookups faster.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7f80277b1eae4d63b4d83054ad407686">

<span data-offset-key="7f80277b1eae4d63b4d83054ad407686:0">`CURL_LOCK_DATA_SSL_SESSION`</span>

<span data-offset-key="7f80277b1eae4d63b4d83054ad407686:1"> - the SSL session ID cache is where libcurl store resume information for SSL connections to be able to resume a previous connection faster.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6d87b9dc17274bada5db17c3522b1630">

<span data-offset-key="6d87b9dc17274bada5db17c3522b1630:0">`CURL_LOCK_DATA_CONNECT`</span>

<span data-offset-key="6d87b9dc17274bada5db17c3522b1630:1"> - when set, this handle will use a shared connection cache and thus will probably be more likely to find existing connections to re-use etc, which may result in faster performance when doing multiple transfers to the same host in a serial manner.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="3102477c82c34ef7afc037ad61177ab6">

<span data-offset-key="3102477c82c34ef7afc037ad61177ab6:0">Locking</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8ad1f0c7deb0410b8d69a9fee0db9712">

<span data-offset-key="8ad1f0c7deb0410b8d69a9fee0db9712:0">If you want have the share object shared by transfers in a multi-threaded environment. Perhaps you have a CPU with many cores and you want each core to run its own thread and transfer data, but you still want the different transfers to share data. Then you need to set the mutex callbacks.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="228e3234de224dd1b1f85e76eb490c5e">

<span data-offset-key="228e3234de224dd1b1f85e76eb490c5e:0">If you do not use threading and you </span>

<span data-offset-key="228e3234de224dd1b1f85e76eb490c5e:1">_know_</span>

<span data-offset-key="228e3234de224dd1b1f85e76eb490c5e:2"> you access the shared object in a serial one-at-a-time manner you do not need to set any locks. But if there is ever more than one transfer that access share object at a time, it needs to get mutex callbacks setup to prevent data destruction and possibly even crashes.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4622770b87144dbfaba50b444ea55254">

<span data-offset-key="4622770b87144dbfaba50b444ea55254:0">Since libcurl itself does not know how to lock things or even what threading model you are using, you must make sure to do mutex locks that only allows one access at a time. A lock callback for a pthreads-using application could look similar to:</span>

</span>

</span> static void lock_cb(CURL *handle, curl_lock_data data, curl_lock_access access, void *userptr){ pthread_mutex_lock(&lock[data]); /_ uses a global lock array _/}curl_share_setopt(share, CURLSHOPT_LOCKFUNC, lock_cb);<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8c7fb5ed615b4e479cef81d46803378a">

<span data-offset-key="8c7fb5ed615b4e479cef81d46803378a:0">With the corresponding unlock callback could look like:</span>

</span>

</span> static void unlock_cb(CURL *handle, curl_lock_data data, void *userptr){ pthread_mutex_unlock(&lock[data]); /_ uses a global lock array _/}curl_share_setopt(share, CURLSHOPT_UNLOCKFUNC, unlock_cb);<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="15056bf07f654ea896902d84ab75caee">

<span data-offset-key="15056bf07f654ea896902d84ab75caee:0">Unshare</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="3bf39672a46a448987db47adffbb8932">

<span data-offset-key="3bf39672a46a448987db47adffbb8932:0">A transfer will use the share object during its transfer and share what that object has been specified to share with other handles sharing the same object.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f94dd9fda6194f0bbf8049d8cebac456">

<span data-offset-key="f94dd9fda6194f0bbf8049d8cebac456:0">In a subsequent transfer, </span>

<span data-offset-key="f94dd9fda6194f0bbf8049d8cebac456:1">`CURLOPT_SHARE`</span>

<span data-offset-key="f94dd9fda6194f0bbf8049d8cebac456:2"> can be set to NULL to prevent a transfer from continuing to share. It that case, the handle may start the next transfer with empty caches for the data that was previously shared.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7207ae6e85a54b5092ff175331f29cf1">

<span data-offset-key="7207ae6e85a54b5092ff175331f29cf1:0">Between two transfers, a share object can also get updated to share a different set of properties so that the handles that share that object will share a different set of data next time. You remove an item to share from a shared object with the curl_share_setopt()'s </span>

<span data-offset-key="7207ae6e85a54b5092ff175331f29cf1:1">`CURLSHOPT_UNSHARE`</span>

<span data-offset-key="7207ae6e85a54b5092ff175331f29cf1:2"> option like this when unsharing DNS data:</span>

</span>

</span> curl_share_setopt(share, CURLSHOPT_UNSHARE, CURL_LOCK_DATA_DNS);<a href="getinfo.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Post transfer info</span>

<a href="url.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">URL API</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 1 year ago</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="sharing.html#multi-handle" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Multi handle</span>

</span>

<a href="sharing.html#sharing-between-easy-handles" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Sharing between easy handles</span>

</span>

<a href="sharing.html#what-to-share" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">What to share</span>

</span>

<a href="sharing.html#locking" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Locking</span>

</span>

<a href="sharing.html#unshare" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Unshare</span>

</span>
