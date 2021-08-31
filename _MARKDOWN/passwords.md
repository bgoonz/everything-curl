<a href="../index.html" class="link-a079aa82--primary-53a25e66--logoLink-10d08504"></a>

<img src="https://gblobscdn.gitbook.com/orgs%2F-LxuH0qSm4xO9nWfEBlB%2Favatar.png?alt=media" class="image-67b14f24--avatar-1c1d03ec" />

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1--spaceNameText-677c2969">Everything curl</span>

<a href="../index.html" class="link-a079aa82--primary-53a25e66--logoLink-10d08504"></a>

<img src="https://gblobscdn.gitbook.com/orgs%2F-LxuH0qSm4xO9nWfEBlB%2Favatar.png?alt=media" class="image-67b14f24--avatar-1c1d03ec" />

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1--spaceNameText-677c2969">Everything curl</span>

<a href="../index.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Introduction</span></a>

<a href="../how-to-read.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">How to read this book</span></a>



<a href="options.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Command line options</span></a>

<a href="versions.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Options depend on version</span></a>

<a href="urls.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">URLs</span></a>

<a href="globbing.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">URL globbing</span></a>

<a href="listopts.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">List options</span></a>

<a href="configfile.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Config file</span></a>

<a href="passwords.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Passwords</span></a>

<a href="progressmeter.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Progress meter</span></a>



<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">How to HTTP with curl</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">libcurl basics</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP with libcurl</span>

<a href="../bindings.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Bindings</span></a>

<a href="../internals.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">libcurl internals</span></a>

<a href="../bookindex.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f"></span></a>





# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Passwords</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2"></span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2"></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="4e5aec8bb68d4f1fa789acb0aaf1b3d6"><span data-offset-key="4e5aec8bb68d4f1fa789acb0aaf1b3d6:0">Passwords are tricky and sensitive. Leaking a password can make someone other than you access the resources and the data otherwise protected.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="911f7e46a4334d6897e304e635810406"><span data-offset-key="911f7e46a4334d6897e304e635810406:0">curl offers several ways to receive passwords from the user and then subsequently pass them on or use them to something else.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="1908b397f25744b9a1b13155e063a26b"><span data-offset-key="1908b397f25744b9a1b13155e063a26b:0">The most basic curl authentication option is </span><span data-offset-key="1908b397f25744b9a1b13155e063a26b:1">`-u / --user`</span><span data-offset-key="1908b397f25744b9a1b13155e063a26b:2">. It accepts an argument that is the user name and password, colon separated. Like when alice wants to request a page requiring HTTP authentication and her password is '12345':</span></span></span>

    $ curl -u alice:12345 http://example.com/

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="4699a94404934c8191048225eba10285"><span data-offset-key="4699a94404934c8191048225eba10285:0">Command line leakage</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="58d919a480bc4d528091215e54b9c571"><span data-offset-key="58d919a480bc4d528091215e54b9c571:0">Several potentially bad things are going on here. First, we are entering a password on the command line and the command line might be readable for other users on the same system (assuming you have a multi-user system). curl will help minimize that risk by trying to blank out passwords from process listings.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="07e7c8bde2ed4af9a875a6987a785a47"><span data-offset-key="07e7c8bde2ed4af9a875a6987a785a47:0">One way to avoid passing the user name and password on the command line is to instead use a </span></span><a href="../usingcurl/netrc.html" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="97559396061c4b7dbacd0f1677067b99"><span data-offset-key="97559396061c4b7dbacd0f1677067b99:0">.netrc file</span></span></a><span data-key="b3e8fc630a2e4d2fa83ae8bd74d0a9d6"><span data-offset-key="b3e8fc630a2e4d2fa83ae8bd74d0a9d6:0"> or a </span></span><a href="configfile.html" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="a2f9494dce6244ffa10020e5fbc4226a"><span data-offset-key="a2f9494dce6244ffa10020e5fbc4226a:0">config file</span></span></a><span data-key="4f0298a2ece74083802a34e7f3e28bf1"><span data-offset-key="4f0298a2ece74083802a34e7f3e28bf1:0">. You can also use the </span><span data-offset-key="4f0298a2ece74083802a34e7f3e28bf1:1">`-u`</span><span data-offset-key="4f0298a2ece74083802a34e7f3e28bf1:2"> option without specifying the password, and then curl will instead prompt the user for it when it runs.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="c4492c6945b04b4e8aff397aea2245e9"><span data-offset-key="c4492c6945b04b4e8aff397aea2245e9:0">Network leakage</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="2234330dfa9244b4a001baf77e26a840"><span data-offset-key="2234330dfa9244b4a001baf77e26a840:0">Secondly, this command line sends the user credentials to an HTTP server, which is a clear-text protocol that is open for man-in-the-middle or other snoopers to spy on the connection and see what is sent. In this command line example, it makes curl use HTTP Basic authentication and that is completely insecure.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="77ac62d24c194139ba2cc19bb7744059"><span data-offset-key="77ac62d24c194139ba2cc19bb7744059:0">There are several ways to avoid this, and the key is, of course, then to avoid protocols or authentication schemes that sends credentials in plain text over the network. Easiest is perhaps to make sure you use encrypted versions of protocols. Use HTTPS instead of HTTP, use FTPS instead of FTP and so on.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="812b9649bb7f4f46b60321cc7dad64ba"><span data-offset-key="812b9649bb7f4f46b60321cc7dad64ba:0">If you need to stick to a plain text and insecure protocol, then see if you can switch to using an authentication method that avoids sending the credentials in the clear. If you want HTTP, such methods would include Digest (</span><span data-offset-key="812b9649bb7f4f46b60321cc7dad64ba:1">`--digest`</span><span data-offset-key="812b9649bb7f4f46b60321cc7dad64ba:2">), Negotiate (</span><span data-offset-key="812b9649bb7f4f46b60321cc7dad64ba:3">`--negotiate.`</span><span data-offset-key="812b9649bb7f4f46b60321cc7dad64ba:4">) and NTLM (</span><span data-offset-key="812b9649bb7f4f46b60321cc7dad64ba:5">`--ntlm`</span><span data-offset-key="812b9649bb7f4f46b60321cc7dad64ba:6">).</span></span></span>

<a href="configfile.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674"></a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Config file</span>

<a href="progressmeter.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42"></a>


<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Progress meter</span>



<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 1 year ago</span>



<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="passwords.html#command-line-leakage" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Command line leakage</span></span>

<a href="passwords.html#network-leakage" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Network leakage</span></span>
