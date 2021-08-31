<a href="../layout.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="../options.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="../style.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="../contributing.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="../reportvuln.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="../web.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="fromsource.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Build from source</span>

</a>

<a href="deps.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Dependencies</span>

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">TLS libraries</span>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Build from source</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7b39ac8c35c941d2a53e625b46aade74">

<span data-offset-key="7b39ac8c35c941d2a53e625b46aade74:0">The curl project creates source code that can be built to produce the two products curl and libcurl. The conversion from source code to binaries is often referred to as "building". You build curl and libcurl from source.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="fa7db45c11674afa85c9732ed3ce78ca">

<span data-offset-key="fa7db45c11674afa85c9732ed3ce78ca:0">The curl project does not provide any built binaries at all, it only ships the source code. The binaries which can be found on the download page of the curl web and installed from other places on the Internet are all built and provided to the world by other friendly people and organizations.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e8abdcaee8534555843e1eab3f29e674">

<span data-offset-key="e8abdcaee8534555843e1eab3f29e674:0">The source code consists of a large number of files containing C code. Generally speaking, the same set of files are used to build binaries for all platforms and computer architectures that curl supports. curl can be built and run on a vast number of platforms. If you use a rare operating system yourself, chances are that building curl from source is the easiest or perhaps the only way to get curl.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7a5b5d604669437891c2b3d8623173b5">

<span data-offset-key="7a5b5d604669437891c2b3d8623173b5:0">Making it easy to build curl is a priority to the curl project, although we do not always necessarily succeed!</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="52c6e523c5ab449daafd7277d6698871">

<span data-offset-key="52c6e523c5ab449daafd7277d6698871:0">git vs tarballs</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="99509f42302d4fa3a91401ef20320502">

<span data-offset-key="99509f42302d4fa3a91401ef20320502:0">When release tarballs are created, a few files are generated and included in the final release file. Those generated files are not present in the git repository, because they are generated and there is no need to store them in git.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0bcb985488a24244aa88840ce1c693fc">

<span data-offset-key="0bcb985488a24244aa88840ce1c693fc:0">So, if you want to build curl from git you need to generate some of those files yourself before you can build. On Linux and Unix-like systems, do this by running </span>

<span data-offset-key="0bcb985488a24244aa88840ce1c693fc:1">`./buildconf`</span>

<span data-offset-key="0bcb985488a24244aa88840ce1c693fc:2"> and on Windows you run </span>

<span data-offset-key="0bcb985488a24244aa88840ce1c693fc:3">`buildconf.bat`</span>

<span data-offset-key="0bcb985488a24244aa88840ce1c693fc:4">.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="9a464061e99c43f9a40c2abcdd923226">

<span data-offset-key="9a464061e99c43f9a40c2abcdd923226:0">On Linux and Unix-like systems</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7c4d7f517b514600af49765f5b0f0c42">

<span data-offset-key="7c4d7f517b514600af49765f5b0f0c42:0">There are two distinctly different ways to build curl on Linux and other Unix-like systems. There's the one using the configure script and there's the CMake approach.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="86d1a40cc7ac46ab871ce426e3708915">

<span data-offset-key="86d1a40cc7ac46ab871ce426e3708915:0">There are two different build environments to cater for people's different opinions and tastes. The configure based build is arguably the more mature and more covering build system and should probably be considered the default one.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="941fa6c2987c4c8a98fb2f9c04e282eb">

<span data-offset-key="941fa6c2987c4c8a98fb2f9c04e282eb:0">Autotools</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9086f66933c340d698d8ea328f25a035">

<span data-offset-key="9086f66933c340d698d8ea328f25a035:0">The "Autotools" is a collection of different tools that used together generate the </span>

<span data-offset-key="9086f66933c340d698d8ea328f25a035:1">`configure`</span>

<span data-offset-key="9086f66933c340d698d8ea328f25a035:2"> script. The configure script is run by the user who wants to build curl and it does a whole bunch of things:</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0b2ef51ce8ab4738bd442840f3b9b8aa">

<span data-offset-key="0b2ef51ce8ab4738bd442840f3b9b8aa:0">it checks for features and functions present in your system</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c83700a68b9a447890e48bb03d59f374">

<span data-offset-key="c83700a68b9a447890e48bb03d59f374:0">it offers command-line options so that you as a builder can decide what to enable and disable in the build. Features and protocols, etc., can be toggled on/off. Or even compiler warning levels and more.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b827eeca4ac94c33a98584a403467ce5">

<span data-offset-key="b827eeca4ac94c33a98584a403467ce5:0">it offers command-line options to let the builder point to specific installation paths for various third-party dependencies that curl can be built to use.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="134a73b70edd4fa4a77e48ceca7470f2">

<span data-offset-key="134a73b70edd4fa4a77e48ceca7470f2:0">specifies on which file path the generated installation should be placed when ultimately the build is made and "make install" is invoked</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="befa0c4d348c4fbab9728f2ef904930c">

<span data-offset-key="befa0c4d348c4fbab9728f2ef904930c:0">In the most basic usage, just running </span>

<span data-offset-key="befa0c4d348c4fbab9728f2ef904930c:1">`./configure`</span>

<span data-offset-key="befa0c4d348c4fbab9728f2ef904930c:2"> in the source directory is enough. When the script completes, it outputs a summary of what options it has detected/enabled and what features that are still disabled, some of them possibly because it failed to detect the presence of necessary third-party dependencies that are needed for those functions to work. If the summary is not what you expected it to be, invoke configure again with new options or with the previously used options adjusted.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="5bb9593923624cf89111c2f6ab08e126">

<span data-offset-key="5bb9593923624cf89111c2f6ab08e126:0">After configure has completed you invoke </span>

<span data-offset-key="5bb9593923624cf89111c2f6ab08e126:1">`make`</span>

<span data-offset-key="5bb9593923624cf89111c2f6ab08e126:2"> to build the entire thing and then finally </span>

<span data-offset-key="5bb9593923624cf89111c2f6ab08e126:3">`make install`</span>

<span data-offset-key="5bb9593923624cf89111c2f6ab08e126:4"> to install curl, libcurl and associated things. </span>

<span data-offset-key="5bb9593923624cf89111c2f6ab08e126:5">`make install`</span>

<span data-offset-key="5bb9593923624cf89111c2f6ab08e126:6"> requires that you have the correct rights in your system to create and write files in the installation directory or you will get some errors.</span>

</span>

</span>

<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="c944133f1fc74014a94bd6ac8e497d21">

<span data-offset-key="c944133f1fc74014a94bd6ac8e497d21:0">cross-compiling</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="52059004d9a24664ab91d785124de8f8">

<span data-offset-key="52059004d9a24664ab91d785124de8f8:0">Cross-compiling means that you build the source on one architecture but the output is created to be run on a different one. For example, you could build the source on a Linux machine but have the output work to run on a Windows machine.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="649aea37051a4c299bb8ab449fb6f1d7">

<span data-offset-key="649aea37051a4c299bb8ab449fb6f1d7:0">For cross-compiling to work, you need a dedicated compiler and build system setup for the particular target system for which you want to build. How to get and install that system is not covered in this book.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="786bc1d0c8894fb7835984c593ad0b8a">

<span data-offset-key="786bc1d0c8894fb7835984c593ad0b8a:0">Once you have a cross compiler, you can instruct configure to use that compiler instead of the "native" compiler when it builds curl so that the end result then can be moved over and used on the other machine.</span>

</span>

</span>

<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="74a3fb4c44dd4dbf886231306cb41968">

<span data-offset-key="74a3fb4c44dd4dbf886231306cb41968:0">static linking</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="aecfeef171654463981b7929119599ec">

<span data-offset-key="aecfeef171654463981b7929119599ec:0">By default, configure will setup the build files so that the following 'make' command will create both shared and static versions of libcurl. You can change that with the </span>

<span data-offset-key="aecfeef171654463981b7929119599ec:1">`--disable-static`</span>

<span data-offset-key="aecfeef171654463981b7929119599ec:2"> or </span>

<span data-offset-key="aecfeef171654463981b7929119599ec:3">`--disable-shared`</span>

<span data-offset-key="aecfeef171654463981b7929119599ec:4"> options to configure.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="dbeb66b828fb4f0aa02a796a012f0b90">

<span data-offset-key="dbeb66b828fb4f0aa02a796a012f0b90:0">If you instead want to build with static versions of third party libraries instead of shared libraries, you need to prepare yourself for an uphill battle. curl's configure script is focused on setting up and building with shared libraries.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="25188ec446d146a1ad7751712a8e5661">

<span data-offset-key="25188ec446d146a1ad7751712a8e5661:0">One of the differences between linking with a static library compared to linking with a shared one is in how shared libraries handle their own dependencies while static ones do not. In order to link with library xyz as a shared library, it is as bsically a matter of adding </span>

<span data-offset-key="25188ec446d146a1ad7751712a8e5661:1">`-lxyz`</span>

<span data-offset-key="25188ec446d146a1ad7751712a8e5661:2"> to the linker command line no matter which other libraries xyz itself was built to use, but if that xyz is instead a static library we also need to specify each of xyz's dependencies on the linker command line. curl's configure typically cannot keep up with or know all possible dependencies for all the libraries it can be made to build with, so users wanting to build with static libs mostly need to provide that list of libraries to link with.</span>

</span>

</span>

<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="48464878596b49be838464ff67513db2">

<span data-offset-key="48464878596b49be838464ff67513db2:0">Select TLS backend</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="bde3e0ed4530483e9c2d98535e0801e8">

<span data-offset-key="bde3e0ed4530483e9c2d98535e0801e8:0">The configure based build offers the user to select from a wide variety of different TLS libraries when building. You select them by using the correct command line options.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9644a630a329451ea1b4aac9892442e7">

<span data-offset-key="9644a630a329451ea1b4aac9892442e7:0">The default OpenSSL configure check will also detect and use BoringSSL or libressl.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0f1641dea43a4f4895f3da0eca53f3bf">

<span data-offset-key="0f1641dea43a4f4895f3da0eca53f3bf:0">BearSSL: </span>

<span data-offset-key="0f1641dea43a4f4895f3da0eca53f3bf:1">`--without-ssl --with-bearssl`</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="127b0a902cbe4a058ac102e1761c2879">

<span data-offset-key="127b0a902cbe4a058ac102e1761c2879:0">BoringSSL: - by default</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0e0439b069424044ac14be6f3a9c1bc8">

<span data-offset-key="0e0439b069424044ac14be6f3a9c1bc8:0">GnuTLS: </span>

<span data-offset-key="0e0439b069424044ac14be6f3a9c1bc8:1">`--without-ssl --with-gnutls`</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="494121bc49634947ba2247d27137af1c">

<span data-offset-key="494121bc49634947ba2247d27137af1c:0">MesaLink: </span>

<span data-offset-key="494121bc49634947ba2247d27137af1c:1">`--without-ssl --with-mesalink`</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9dda6652cea74e309d6929498a0ffd1e">

<span data-offset-key="9dda6652cea74e309d6929498a0ffd1e:0">NSS: </span>

<span data-offset-key="9dda6652cea74e309d6929498a0ffd1e:1">`--without-ssl --with-nss`</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="eddb6a70ea184682bbb055ae020df8cd">

<span data-offset-key="eddb6a70ea184682bbb055ae020df8cd:0">OpenSSL: - by default</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="74e9c74ec8a64db39eb4b80ed1880601">

<span data-offset-key="74e9c74ec8a64db39eb4b80ed1880601:0">PolarSSL: </span>

<span data-offset-key="74e9c74ec8a64db39eb4b80ed1880601:1">`--without-ssl --with-polarssl`</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="402c3956611245128ee693b090444570">

<span data-offset-key="402c3956611245128ee693b090444570:0">Wolfssl: </span>

<span data-offset-key="402c3956611245128ee693b090444570:1">`--without-ssl --with-wolfssl`</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c71dd7893b284d94996ee32242e9307f">

<span data-offset-key="c71dd7893b284d94996ee32242e9307f:0">libressl: - by default</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f9b0645b664948a38e1376fc50e24e8d">

<span data-offset-key="f9b0645b664948a38e1376fc50e24e8d:0">mbedTLS: </span>

<span data-offset-key="f9b0645b664948a38e1376fc50e24e8d:1">`--without-ssl --with-mbedtls`</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0f998645f7b14f4fbdd0f9d57dd3fdb5">

<span data-offset-key="0f998645f7b14f4fbdd0f9d57dd3fdb5:0">schannel: </span>

<span data-offset-key="0f998645f7b14f4fbdd0f9d57dd3fdb5:1">`--without-ssl --with-winssl`</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f45405d3f22648508a5bfe5595f984db">

<span data-offset-key="f45405d3f22648508a5bfe5595f984db:0">secure transport: </span>

<span data-offset-key="f45405d3f22648508a5bfe5595f984db:1">`--with-winssl --with-darwinssl`</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="196743626fe94822968862a4cbf56570">

<span data-offset-key="196743626fe94822968862a4cbf56570:0">All the </span>

<span data-offset-key="196743626fe94822968862a4cbf56570:1">`--with-*`</span>

<span data-offset-key="196743626fe94822968862a4cbf56570:2"> options also allow you to provide the install prefix so that configure will search for the specific library where you tell it to.</span>

</span>

</span>

<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="f85bb782f9a84b6f89b74858566d9391">

<span data-offset-key="f85bb782f9a84b6f89b74858566d9391:0">Select SSH backend</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="668513dffb66458eb042461efc385b1f">

<span data-offset-key="668513dffb66458eb042461efc385b1f:0">The configure based build offers the user to select from a variety of different SSH libraries when building. You select them by using the correct command line options.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="58a6260e8ed44058bec4d601095b823d">

<span data-offset-key="58a6260e8ed44058bec4d601095b823d:0">libssh2: </span>

<span data-offset-key="58a6260e8ed44058bec4d601095b823d:1">`--with-libssh2`</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="fd76c5ecdd5142f89c50d863f726a1f0">

<span data-offset-key="fd76c5ecdd5142f89c50d863f726a1f0:0">libssh: </span>

<span data-offset-key="fd76c5ecdd5142f89c50d863f726a1f0:1">`--with-libssh`</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="83ddfd622f9d4f4fa09bb7c215169712">

<span data-offset-key="83ddfd622f9d4f4fa09bb7c215169712:0">wolfSSH: </span>

<span data-offset-key="83ddfd622f9d4f4fa09bb7c215169712:1">`--with-wolfssh`</span>

</span>

</span>

<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="a774c43c2b1b4d5fa2b27beed7957579">

<span data-offset-key="a774c43c2b1b4d5fa2b27beed7957579:0">Select HTTP/3 backend</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="65e25f64808649e4a68d978cdfadce81">

<span data-offset-key="65e25f64808649e4a68d978cdfadce81:0">The configure based build offers the user to select different HTTP/3 libraries when building. You select them by using the correct command line options.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="792bee02f79f4d4c861e2608354db696">

<span data-offset-key="792bee02f79f4d4c861e2608354db696:0">quiche: </span>

<span data-offset-key="792bee02f79f4d4c861e2608354db696:1">`--with-quiche`</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2fe76ed730b347c6a4ebcf601fb03a5c">

<span data-offset-key="2fe76ed730b347c6a4ebcf601fb03a5c:0">ngtcp2: </span>

<span data-offset-key="2fe76ed730b347c6a4ebcf601fb03a5c:1">`--with-ngtcp2 --with-nghttp3`</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="661972582a6c4b6c879a267f54fee0f4">

<span data-offset-key="661972582a6c4b6c879a267f54fee0f4:0">CMake</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e9283c2328c148408cdedeba364f698d">

<span data-offset-key="e9283c2328c148408cdedeba364f698d:0">CMake is an alternative build method that works on most modern platforms, including Windows. Using this method you first need to have cmake installed on your build machine, invoke cmake to generate the build files and then build. With cmake's </span>

<span data-offset-key="e9283c2328c148408cdedeba364f698d:1">`-G`</span>

<span data-offset-key="e9283c2328c148408cdedeba364f698d:2"> flag, you select which build system to generate files for. See </span>

<span data-offset-key="e9283c2328c148408cdedeba364f698d:3">`cmake --help`</span>

<span data-offset-key="e9283c2328c148408cdedeba364f698d:4"> for the list of "generators" your cmake installation supports.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="32de2c05b6e64f27b4d1943061743123">

<span data-offset-key="32de2c05b6e64f27b4d1943061743123:0">On the cmake command line, in the first argument, you specify where to find the cmake source files. Which is </span>

<span data-offset-key="32de2c05b6e64f27b4d1943061743123:1">`.`</span>

<span data-offset-key="32de2c05b6e64f27b4d1943061743123:2"> (a single dot) if in the same directory.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a26fbfb3b8554606942924be2c8aa81c">

<span data-offset-key="a26fbfb3b8554606942924be2c8aa81c:0">To build on Linux using plain make with CmakeLists.txt in the same directory, you can do:</span>

</span>

</span>    cmake -G "Unix Makefiles" .make<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2f44788b6dbe4d3cbad3e243f52ae428">

<span data-offset-key="2f44788b6dbe4d3cbad3e243f52ae428:0">Or rely on the fact that unix makefiles is the default there:</span>

</span>

</span>    cmake .make<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="94b0b06e7427410482026efd61c89b6e">

<span data-offset-key="94b0b06e7427410482026efd61c89b6e:0">To create a subdir for the build and run make in there:</span>

</span>

</span>    mkdir buildcd buildcmake ..make<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="adc809ce81d040f181b3e3aae29fbd1a">

<span data-offset-key="adc809ce81d040f181b3e3aae29fbd1a:0">On Windows</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="43f85f5afbbc4453991f6c3453a451ef">

<span data-offset-key="43f85f5afbbc4453991f6c3453a451ef:0">You can build curl on Windows in several different ways. We recommend using the MSVC compiler from Microsoft or the free and open source mingw compiler. The build process is however not limited to these.</span>

</span>

</span>

<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="8e9330d239d945ce947e008b3af4a96c">

<span data-offset-key="8e9330d239d945ce947e008b3af4a96c:0">nmake</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9cb4a9dc11dc4c168b0005aaffaf85d8">

<span data-offset-key="9cb4a9dc11dc4c168b0005aaffaf85d8:0">Build with MSVC using the nmake utility like this:</span>

</span>

</span>    cd winbuild<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="97a55400e8c742fa9985a5767851456e">

<span data-offset-key="97a55400e8c742fa9985a5767851456e:0">Decide what options to enable/disable in your build. The </span>

<span data-offset-key="97a55400e8c742fa9985a5767851456e:1">`BUILD.WINDOWS.txt`</span>

<span data-offset-key="97a55400e8c742fa9985a5767851456e:2"> file details them all, but an example command line could look like this (split into several lines for readability):</span>

</span>

</span>    nname WITH_SSL=dll WITH_NGHTTP2=dll ENABLE_IPV6=yes \WITH_ZLIB=dll MACHINE=x64<a href="../build.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Build and install</span>

<a href="deps.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Dependencies</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 8 months ago</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="fromsource.html#git-vs-tarballs" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">git vs tarballs</span>

</span>

<a href="fromsource.html#on-linux-and-unix-like-systems" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">On Linux and Unix-like systems</span>

</span>

<a href="fromsource.html#autotools" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Autotools</span>

</span>

<a href="fromsource.html#cross-compiling" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">cross-compiling</span>

</span>

<a href="fromsource.html#static-linking" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">static linking</span>

</span>

<a href="fromsource.html#select-tls-backend" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Select TLS backend</span>

</span>

<a href="fromsource.html#select-ssh-backend" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Select SSH backend</span>

</span>

<a href="fromsource.html#select-http-3-backend" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">Select HTTP/3 backend</span>

</span>

<a href="fromsource.html#cmake" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">CMake</span>

</span>

<a href="fromsource.html#on-windows" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">On Windows</span>

</span>

<a href="fromsource.html#nmake" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">nmake</span>

</span>
