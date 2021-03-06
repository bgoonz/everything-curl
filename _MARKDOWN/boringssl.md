<a href="../../../index.html" class="link-a079aa82--primary-53a25e66--logoLink-10d08504">

</a>

<a href="../../../index.html" class="link-a079aa82--primary-53a25e66--logoLink-10d08504">

</a>

<a href="../../../index.html" class="navButton-94f2579c--navButtonClickable-161b88ca">

</a>

<a href="../../../how-to-read.html" class="navButton-94f2579c--navButtonClickable-161b88ca">

</a>

<a href="../../layout.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="../../options.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="../../style.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="../../contributing.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="../../reportvuln.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="../../web.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="../fromsource.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Build from source</span>

</a>

<a href="../deps.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Dependencies</span>

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">TLS libraries</span>

<a href="boringssl.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">BoringSSL</span>

</a>

<a href="../../../bindings.html" class="navButton-94f2579c--navButtonClickable-161b88ca">

</a>

<a href="../../../internals.html" class="navButton-94f2579c--navButtonClickable-161b88ca">

</a>

<a href="../../../bookindex.html" class="navButton-94f2579c--navButtonClickable-161b88ca">

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">BoringSSL</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="1cb5d488c24e4c878b3e43a58718ef28">

<span data-offset-key="1cb5d488c24e4c878b3e43a58718ef28:0">build boringssl</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="717d2fad518c40ba98cb0620d7e1dbab">

<span data-offset-key="717d2fad518c40ba98cb0620d7e1dbab:0">$HOME/src is where I put the code in this example. You can pick wherever you like.</span>

</span>

</span> $ cd $HOME/src$ git clone https://boringssl.googlesource.com/boringssl$ cd boringssl$ mkdir build$ cd build$ cmake ..$ make<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="b2796fff2dcf4f41895f2c409a948284">

<span data-offset-key="b2796fff2dcf4f41895f2c409a948284:0">set up the build tree to get detected by curl's configure</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="bcff0642f480402f9c5f647efb5d5c9a">

<span data-offset-key="bcff0642f480402f9c5f647efb5d5c9a:0">In the boringssl source tree root, make sure there's a </span>

<span data-offset-key="bcff0642f480402f9c5f647efb5d5c9a:1">`lib`</span>

<span data-offset-key="bcff0642f480402f9c5f647efb5d5c9a:2"> and an </span>

<span data-offset-key="bcff0642f480402f9c5f647efb5d5c9a:3">`include`</span>

<span data-offset-key="bcff0642f480402f9c5f647efb5d5c9a:4"> dir. The </span>

<span data-offset-key="bcff0642f480402f9c5f647efb5d5c9a:5">`lib`</span>

<span data-offset-key="bcff0642f480402f9c5f647efb5d5c9a:6"> dir should contain the two libs (I made them symlinks into the build dir). The </span>

<span data-offset-key="bcff0642f480402f9c5f647efb5d5c9a:7">`include`</span>

<span data-offset-key="bcff0642f480402f9c5f647efb5d5c9a:8"> dir is already present by default. Make and populate </span>

<span data-offset-key="bcff0642f480402f9c5f647efb5d5c9a:9">`lib`</span>

<span data-offset-key="bcff0642f480402f9c5f647efb5d5c9a:10"> like this (commands issued in the source tree root, not in the </span>

<span data-offset-key="bcff0642f480402f9c5f647efb5d5c9a:11">`build/`</span>

<span data-offset-key="bcff0642f480402f9c5f647efb5d5c9a:12"> subdirectory).</span>

</span>

</span> $ mkdir lib$ cd lib$ ln -s ../build/ssl/libssl.a$ ln -s ../build/crypto/libcrypto.a<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="04207032ee3047a180f58f68e6ee293f">

<span data-offset-key="04207032ee3047a180f58f68e6ee293f:0">configure curl</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e0cf6030d9624c8ab5da6db6d072c798">

<span data-offset-key="e0cf6030d9624c8ab5da6db6d072c798:0">`LIBS=-lpthread ./configure --with-ssl=$HOME/src/boringssl`</span>

<span data-offset-key="e0cf6030d9624c8ab5da6db6d072c798:1"> (where I point out the root of the boringssl tree)</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="fd4315449caa44a59d4ab12e35684e38">

<span data-offset-key="fd4315449caa44a59d4ab12e35684e38:0">Verify that at the end of the configuration, it says it detected BoringSSL to be used.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="0bc5f330a2e547b4badc3472b3d30626">

<span data-offset-key="0bc5f330a2e547b4badc3472b3d30626:0">build curl</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="787aae98e41d444ea205bac7eb2ed2d5">

<span data-offset-key="787aae98e41d444ea205bac7eb2ed2d5:0">Run </span>

<span data-offset-key="787aae98e41d444ea205bac7eb2ed2d5:1">`make`</span>

<span data-offset-key="787aae98e41d444ea205bac7eb2ed2d5:2"> in the curl source tree.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="df0e0850b6154c549ae61b4713b6c200">

<span data-offset-key="df0e0850b6154c549ae61b4713b6c200:0">Now you can install curl normally with </span>

<span data-offset-key="df0e0850b6154c549ae61b4713b6c200:1">`make install`</span>

<span data-offset-key="df0e0850b6154c549ae61b4713b6c200:2"> etc.</span>

</span>

</span>

<a href="../tls.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">TLS libraries</span>

<a href="../../../protocols.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Network and protocols</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="boringssl.html#build-boringssl" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">build boringssl</span>

</span>

<a href="boringssl.html#set-up-the-build-tree-to-get-detected-by-curls-configure" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">set up the build tree to get detected by curl's configure</span>

</span>

<a href="boringssl.html#configure-curl" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">configure curl</span>

</span>

<a href="boringssl.html#build-curl" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">build curl</span>

</span>
