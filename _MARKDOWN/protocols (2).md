<a href="index.html" class="link-a079aa82--primary-53a25e66--logoLink-10d08504"></a>





<a href="index.html" class="link-a079aa82--primary-53a25e66--logoLink-10d08504"></a>





<a href="index.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Introduction</span></a>

<a href="how-to-read.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">How to read this book</span></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">The cURL project</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Get curl</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Open Source</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">The source code</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Network and protocols</span>

<a href="protocols/network.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Networking simplified</span></a>

<a href="protocols/protocols.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Protocols</span></a>

<a href="protocols/curl.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">curl protocols</span></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Command line basics</span>



<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">How to HTTP with curl</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">libcurl basics</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP with libcurl</span>

<a href="bindings.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Bindings</span></a>

<a href="internals.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">libcurl internals</span></a>

<a href="bookindex.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f"></span></a>





# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Network and protocols</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2"></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="36838f380d8f4f16a3eb942bade223c2"><span data-offset-key="36838f380d8f4f16a3eb942bade223c2:0">Before diving in and talking about how to use curl to get things done, let's take a look at what all this networking is and how it works, using simplifications and some minor shortcuts to give an easy overview.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="2396c6a951e546a99d87940bac94bb9d"><span data-offset-key="2396c6a951e546a99d87940bac94bb9d:0">The basics are in the </span></span><a href="protocols/network.html" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="eadfc3225ed441bbbc00a0557265eb00"><span data-offset-key="eadfc3225ed441bbbc00a0557265eb00:0">networking simplified</span></span></a><span data-key="4e4e180a646440448b0f329fb364e9e4"><span data-offset-key="4e4e180a646440448b0f329fb364e9e4:0"> chapter that tries to just draw a simple picture of what networking is from a curl perspective, and the </span></span><a href="protocols/protocols.html" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="3e9a0430f2ea4a92bc3a748ae748bbd7"><span data-offset-key="3e9a0430f2ea4a92bc3a748ae748bbd7:0">protocols</span></span></a><span data-key="909587a47efd4cdfaacce7a56817e2ee"><span data-offset-key="909587a47efd4cdfaacce7a56817e2ee:0"> section which explains what exactly a "protocol" is and how that works.</span></span></span>

<a href="source/build/tls/boringssl.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674"></a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">BoringSSL</span>

<a href="protocols/network.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42"></a>


<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Networking simplified</span>



<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>


