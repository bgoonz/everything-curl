<a href="libcurl-http/responses.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP responses</span>

</a>

<a href="libcurl-http/requests.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP requests</span>

</a>

<a href="libcurl-http/versions.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP versions</span>

</a>

<a href="libcurl-http/ranges.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP ranges</span>

</a>

<a href="libcurl-http/auth.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP authentication</span>

</a>

<a href="libcurl-http/cookies.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Cookies with libcurl</span>

</a>

<a href="libcurl-http/download.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Download</span>

</a>

<a href="libcurl-http/upload.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Upload</span>

</a>

<a href="bindings.html" class="navButton-94f2579c--navButtonClickable-161b88ca">href="bookindex.html" class="navButton-94f2579c--navButtonClickable-161b88ca">

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">HTTP with libcurl</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9df88fd1bbce4812a7ac66f4192fded3">

<span data-offset-key="9df88fd1bbce4812a7ac66f4192fded3:0">HTTP is by far the most commonly used protocol by libcurl users and libcurl offers countless ways of modifying such transfers. See the </span>

</span>

<a href="http/basics.html" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="ecd9de310e3b4567b7331c431a134941">

<span data-offset-key="ecd9de310e3b4567b7331c431a134941:0">HTTP protocol basics</span>

</span>

</a>

<span data-key="07891d7be9d943b5808b30e26a10172d">

<span data-offset-key="07891d7be9d943b5808b30e26a10172d:0"> for some basics on how the HTTP protocol works.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="d0f5591b419748209696498eb8844d05">

<span data-offset-key="d0f5591b419748209696498eb8844d05:0">HTTPS</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="41c035bdda004ca2b5f70190611a2908">

<span data-offset-key="41c035bdda004ca2b5f70190611a2908:0">Doing HTTPS is typically done the same way as for HTTP as the extra security layer and server verification etc is done automatically and transparently by default. Just use the </span>

<span data-offset-key="41c035bdda004ca2b5f70190611a2908:1">`https://`</span>

<span data-offset-key="41c035bdda004ca2b5f70190611a2908:2"> scheme in the URL.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="26093f854f964701ac5cd5c3f58fd612">

<span data-offset-key="26093f854f964701ac5cd5c3f58fd612:0">HTTPS is HTTP with TLS on top. See also the </span>

</span>

<a href="libcurl/options/tlsoptions.html" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="e869280680254f7cbe175087f18fac16">

<span data-offset-key="e869280680254f7cbe175087f18fac16:0">TLS options</span>

</span>

</a>

<span data-key="0a7ea1a256d04335b69af46ec33c6e8b">

<span data-offset-key="0a7ea1a256d04335b69af46ec33c6e8b:0"> section.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="5ef73ca02e43423ba431de5a26755f64">

<span data-offset-key="5ef73ca02e43423ba431de5a26755f64:0">HTTP proxy</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6ac4268c46004f96b9a364d8a8d601d2">

<span data-offset-key="6ac4268c46004f96b9a364d8a8d601d2:0">See </span>

</span>

<a href="libcurl/proxies.html" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="469b2667b41e465aaaf8ac55e709d638">

<span data-offset-key="469b2667b41e465aaaf8ac55e709d638:0">using Proxies with libcurl</span>

</span>

</a>

<span data-key="dcf41749174a4284b79dfe4c82ae68a8">

<span data-offset-key="dcf41749174a4284b79dfe4c82ae68a8:0">

<span data-slate-zero-width="z">​</span>

</span>

</span>

</span>

<a href="libcurl/cplusplus.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">for C++ programmers</span>

<a href="libcurl-http/responses.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">HTTP responses</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="libcurl-http.html#https" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">HTTPS</span>

</span>

<a href="libcurl-http.html#http-proxy" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">HTTP proxy</span>

</span>
