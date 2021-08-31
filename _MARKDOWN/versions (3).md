<a href="../index.html" class="link-a079aa82--primary-53a25e66--logoLink-10d08504"></a>





<a href="../index.html" class="link-a079aa82--primary-53a25e66--logoLink-10d08504"></a>





<a href="../index.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Introduction</span></a>

<a href="../how-to-read.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">How to read this book</span></a>



<a href="options.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Command line options</span></a>

<a href="versions.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Options depend on version</span></a>

<a href="urls.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">URLs</span></a>

<a href="globbing.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">URL globbing</span></a>

<a href="listopts.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">List options</span></a>

<a href="configfile.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Config file</span></a>

<a href="passwords.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Passwords</span></a>

<a href="progressmeter.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Progress meter</span></a>



<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">How to HTTP with curl</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">libcurl basics</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP with libcurl</span>

<a href="../bindings.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Bindings</span></a>

<a href="../internals.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">libcurl internals</span></a>

<a href="../bookindex.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f"></span></a>





# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Options depend on version</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2"></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="6997a9fe65cb438da254e72f99547693"><span data-offset-key="6997a9fe65cb438da254e72f99547693:0">`curl`</span><span data-offset-key="6997a9fe65cb438da254e72f99547693:1"> was first typed on a command line back in the glorious year of 1998. It already then worked on the specified URL and none, one or more command-line options given to it.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="0ebbd74418fd4370bacfa1cca1df979a"><span data-offset-key="0ebbd74418fd4370bacfa1cca1df979a:0">Since then we have added more options. We add options as we go along and almost every new release of curl has one or a few new options that allow users to modify certain aspects of its operation.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="7b1c4460bf7c4daeb4c96c22696f9a4c"><span data-offset-key="7b1c4460bf7c4daeb4c96c22696f9a4c:0">With the curl project's rather speedy release chain with a new release shipping every eight weeks, it is almost inevitable that you are at least not always using the latest released version of curl. Sometimes you may even use a curl version that is a few years old.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="d44a6316afa843279dac68a00aa83278"><span data-offset-key="d44a6316afa843279dac68a00aa83278:0">All command-line options described in this book were, of course, added to curl at some point and only a small portion of them were available that fine spring day in 1998 when curl first shipped. You may have reason to check your version of curl and crosscheck with the curl man page for when certain options were added. This is especially important if you want to take a curl command line using a modern curl version back to an older system that might be running an older installation.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="027d0e390b8b4907b695d14e4579dfcb"><span data-offset-key="027d0e390b8b4907b695d14e4579dfcb:0">The developers of curl are working hard to not change existing behavior. Command lines written to use curl in 1998, 2003 or 2010 should all be possible to run unmodified even today.</span></span></span>

<a href="options.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674"></a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Command line options</span>

<a href="urls.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42"></a>


<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">URLs</span>



<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 1 year ago</span>


