<a href="../index.html" class="link-a079aa82--primary-53a25e66--logoLink-10d08504"></a>

<img src="https://gblobscdn.gitbook.com/orgs%2F-LxuH0qSm4xO9nWfEBlB%2Favatar.png?alt=media" class="image-67b14f24--avatar-1c1d03ec" />

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1--spaceNameText-677c2969">Everything curl</span>

<a href="../index.html" class="link-a079aa82--primary-53a25e66--logoLink-10d08504"></a>

<img src="https://gblobscdn.gitbook.com/orgs%2F-LxuH0qSm4xO9nWfEBlB%2Favatar.png?alt=media" class="image-67b14f24--avatar-1c1d03ec" />

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1--spaceNameText-677c2969">Everything curl</span>

<a href="../index.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Introduction</span></a>

<a href="../how-to-read.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">How to read this book</span></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">The cURL project</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Get curl</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Open Source</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">The source code</span>

<a href="layout.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Code layout</span></a>

<a href="options.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Handling build options</span></a>

<a href="style.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Code style</span></a>

<a href="contributing.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Contributing</span></a>

<a href="reportvuln.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Reporting vulnerabilities</span></a>

<a href="web.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Web site</span></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Build and install</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Network and protocols</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Command line basics</span>



<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">How to HTTP with curl</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">libcurl basics</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP with libcurl</span>

<a href="../bindings.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Bindings</span></a>

<a href="../internals.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">libcurl internals</span></a>

<a href="../bookindex.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f"></span></a>





# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Handling build options</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2"></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="59172c60016c4beba94e9286b5b8d867"><span data-offset-key="59172c60016c4beba94e9286b5b8d867:0">The curl and libcurl source code have been carefully written to build and run on virtually every computer platform in existence. This can only be done through hard work and by adhering to a few guidelines (and, of course, a fair amount of testing).</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="9419c8e1a98f4c08a6bb417565d8b435"><span data-offset-key="9419c8e1a98f4c08a6bb417565d8b435:0">A golden rule is to always add \#ifdefs that checks for specific features, and then have the setup scripts (configure or CMake or hard-coded) check for the presence of said features in a user's computer setup before the program is compiled there. Additionally and as a bonus, thanks to this way of writing the code, some features can be explicitly turned off even if they are present in the system and </span><span data-offset-key="9419c8e1a98f4c08a6bb417565d8b435:1">_could_</span><span data-offset-key="9419c8e1a98f4c08a6bb417565d8b435:2"> be used. Examples of that would be when users want to, for example, build a version of the library with a smaller footprint or with support for certain protocols disabled, etc.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="073e02c720774665aeaeebed508ef4d5"><span data-offset-key="073e02c720774665aeaeebed508ef4d5:0">The project sometimes uses \#ifdef protection around entire source files when, for example, a single file is provided for a specific operating system or perhaps for a specific feature that is not always present. This is to make it possible for all platforms to always build all files—it simplifies the build scripts and makefiles a lot. A file entirely \#ifdefed out hardly adds anything to the build time, anyway.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="a1364653cf8e4fed94ff649e36c7fcc0"><span data-offset-key="a1364653cf8e4fed94ff649e36c7fcc0:0">Rather than sprinkling the code with \#ifdefs, to the extent where it is possible, we provide functions and macros that make the code look and work the same, independent of present features. Some of those are then empty macros for the builds that lack the features.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="7688710ebf7844a7a4d449baf6a7bb8f"><span data-offset-key="7688710ebf7844a7a4d449baf6a7bb8f:0">Both TLS handling and name resolving are handled with an internal API that hides the specific implementation and choice of 3rd party software library. That way, most of the internals work the same independent of which TLS library or name resolving system libcurl is told to use.</span></span></span>

<a href="layout.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674"></a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Code layout</span>

<a href="style.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42"></a>


<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Code style</span>



<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>


