<a href="index.html" class="link-a079aa82--primary-53a25e66--logoLink-10d08504"></a>





<a href="index.html" class="link-a079aa82--primary-53a25e66--logoLink-10d08504"></a>





<a href="index.html" class="navButton-94f2579c--navButtonClickable-161b88ca--navButtonOpened-6a88552e"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Introduction</span></a>

<a href="how-to-read.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">How to read this book</span></a>





<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">How to HTTP with curl</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">libcurl basics</span>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">HTTP with libcurl</span>

<a href="bindings.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Bindings</span></a>

<a href="internals.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">libcurl internals</span></a>

<a href="bookindex.html" class="navButton-94f2579c--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f"></span></a>





# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Introduction</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2"></span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2"></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="c850d034709e428cae4b32969307c325"><span data-offset-key="c850d034709e428cae4b32969307c325:0">_Everything curl_</span><span data-offset-key="c850d034709e428cae4b32969307c325:1"> is an extensive guide for all things curl. The project, the command-line tool, the library, how everything started and how it came to be the useful tool it is today.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="4895bd62b2dc40d289076043df05b99e"><span data-offset-key="4895bd62b2dc40d289076043df05b99e:0">This guide explains how we work on developing it further, what it takes to use it, how you can contribute with code or bug reports and why millions of existing users use it.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="ade032317f4b482aa797ba6a65819125"><span data-offset-key="ade032317f4b482aa797ba6a65819125:0">This book is meant to be interesting and useful to both casual readers and somewhat more experienced developers. It offers something for everyone to pick and choose from.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="063fd3f41f194512b4153ae9bb7d13e1"><span data-offset-key="063fd3f41f194512b4153ae9bb7d13e1:0">Do not try to read it from front to back. Read the chapters or content you are curious about and flip back and forth as you see fit.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="3173dea1a941499fbaedb872dca6b4ac"><span data-offset-key="3173dea1a941499fbaedb872dca6b4ac:0">I hope to run this book project as I do all other projects I work on: in the open, completely free to download and read. I want it to be free for anyone to comment on, and available for everyone to contribute to and help out with.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="b627127cb59a4176b9061fa1690af56c"><span data-offset-key="b627127cb59a4176b9061fa1690af56c:0">Send your bug reports, pull requests or critiques to me and I will improve this book accordingly.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="2725c05ec99a4275bd73ea0802039a80"><span data-offset-key="2725c05ec99a4275bd73ea0802039a80:0">This book will never be finished. I intend to keep working on it. While I may at some point consider it fairly complete, covering most aspects of the project (even if only that seems like an insurmountable goal), the curl project will continue to move so there will always be things to update in the book as well.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="f2a41d0a57264d57ba3fd00968560982"><span data-offset-key="f2a41d0a57264d57ba3fd00968560982:0">This book project started at the end of September 2015.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="4116192b5bb74241aa3399681ca74206"><span data-offset-key="4116192b5bb74241aa3399681ca74206:0">The book sites</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="954edac7eed344d98422ec1608fd9562"><span data-offset-key="954edac7eed344d98422ec1608fd9562:0"><span data-slate-zero-width="z">​</span></span></span><a href="index.html" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="d7157918e7584688870a249b62c70ecd"><span data-offset-key="d7157918e7584688870a249b62c70ecd:0">https://everything.curl.dev</span></span></a><span data-key="5e5722a7acc64ceea4cb452e2e1d56ec"><span data-offset-key="5e5722a7acc64ceea4cb452e2e1d56ec:0"> is the home of this book. It features accessible links to read the book online in a web version, or download a PDF version for offline reading. Unfortunately, the previously provided ebook formats are no longer provided by gitbook.com that we use to produce the book.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="129a7a94f256493e981a658ab858f96a"><span data-offset-key="129a7a94f256493e981a658ab858f96a:0"><span data-slate-zero-width="z">​</span></span></span><a href="https://github.com/bagder/everything-curl" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="b6c1fc36790f49a6956e88b743ff1bbe"><span data-offset-key="b6c1fc36790f49a6956e88b743ff1bbe:0">https://github.com/bagder/everything-curl</span></span></a><span data-key="c612c96479724a5aba01c387811501d2"><span data-offset-key="c612c96479724a5aba01c387811501d2:0"> hosts all the book content.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="172da1eaa4c5432f8d5a53a69793b643"><span data-offset-key="172da1eaa4c5432f8d5a53a69793b643:0">The author</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="842cebf9336d4e84995a6a5cfcf5127b"><span data-offset-key="842cebf9336d4e84995a6a5cfcf5127b:0">With the hope of becoming just a co-author of this material, I am Daniel Stenberg. I founded the curl project and I'm a developer at heart—for fun and profit. I live and work in Stockholm, Sweden.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="15650e33123443c6b7af7086892fab87"><span data-offset-key="15650e33123443c6b7af7086892fab87:0">All there is to know about me can be found on </span></span><a href="https://daniel.haxx.se/" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="e89991354fa74c0a8ea4bcad3f2901ad"><span data-offset-key="e89991354fa74c0a8ea4bcad3f2901ad:0">my web site</span></span></a><span data-key="7fbf1dad63c841cf8b7d93f24916356a"><span data-offset-key="7fbf1dad63c841cf8b7d93f24916356a:0">.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="372c7cd1f8464d1e9146e06dfd8873d4"><span data-offset-key="372c7cd1f8464d1e9146e06dfd8873d4:0">Help</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="e54ac37f109c47889227436c955658ba"><span data-offset-key="e54ac37f109c47889227436c955658ba:0">If you find mistakes, omissions, errors or blatant lies in this document, please send me a refreshed version of the affected paragraph and I will make amended versions. I will give proper credits to everyone who helps out! I hope to make this document better over time.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="44c96297130f4c0fa751c9d56df73ca9"><span data-offset-key="44c96297130f4c0fa751c9d56df73ca9:0">Preferably, you could submit </span></span><a href="https://github.com/bagder/everything-curl/issues" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="ebd69ed3660941abb1e1c34f64d26efe"><span data-offset-key="ebd69ed3660941abb1e1c34f64d26efe:0">errors</span></span></a><span data-key="b2cb1bfb6a0c4800b02e71f02f153b4c"><span data-offset-key="b2cb1bfb6a0c4800b02e71f02f153b4c:0"> or </span></span><a href="https://github.com/bagder/everything-curl/pulls" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="d93c5778a0bc4b0fb933cc53e292f809"><span data-offset-key="d93c5778a0bc4b0fb933cc53e292f809:0">pull requests</span></span></a><span data-key="e74ba8a57ef040ec9af6169a9c79fe91"><span data-offset-key="e74ba8a57ef040ec9af6169a9c79fe91:0"> on the book's GitHub page.</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="c93c14a2f5cc47929f0b2a2ef2ae9653"><span data-offset-key="c93c14a2f5cc47929f0b2a2ef2ae9653:0">Helpers</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="2a8ee6b7b5b14b0da8af8ce5c83e6b33"><span data-offset-key="2a8ee6b7b5b14b0da8af8ce5c83e6b33:0">Lots of people have reported bugs, improved sections or otherwise helped making this book the success it is. These friends include the following:</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="b723c28541204f72b891425b15fb2bad"><span data-offset-key="b723c28541204f72b891425b15fb2bad:0">AaronChen0 on github, alawvt on github, Amin Khoshnood, amnkh on github, Anders Roxell, Angad Gill, Aris (Karim) Merchant, Ben Bodenmiller, Ben Peachey, bookofportals on github, Carlton Gibson, Chris DeLuca, Citizen Esosa, Dan Fandrich, Daniel Sabsay, David Piano, DrDoom74 at GitHub, Emil Hessman, enachos71 on github, ethomag on github, Frank Dana, Frank Hassanabad, Gautham B A, Geir Hauge, Helena Udd, Hubert Lin, i-ky on github, infinnovation-dev on GitHub, Jay Ottinger, Jay Satiro, John Simpson, JohnCoconut on github, JoyIfBam5, lowttl on github, Luca Niccoli, Manuel on github, Marius Žilėnas, Mark Koester, Martin van den Nieuwelaar, mehandes on github, Michael Kaufmann, Ms2ger, Nick Travers, Nicolas Brassard, Oscar on github, Patrik Lundin, Ryan McQuen, Saravanan Musuwathi Kesavan, Senthil Kumaran, Shusen Liu, Spiros Georgaras, Stephen, Steve Holme, strupo on github, Viktor Szakats, Vitaliy T, Wayne Lai Wieland Hoffmann, 谭九鼎</span></span></span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="d4e1489070424163a3a671e60116c832"><span data-offset-key="d4e1489070424163a3a671e60116c832:0">License</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="0d9afd0819ce4ca9bd1a40acd88a76a1"><span data-offset-key="0d9afd0819ce4ca9bd1a40acd88a76a1:0">This document is licensed under the </span></span><a href="https://creativecommons.org/licenses/by/4.0/" class="link-a079aa82--primary-53a25e66--link-faf6c434"><span data-key="0de9f984586249299a124f6802b4b28b"><span data-offset-key="0de9f984586249299a124f6802b4b28b:0">Creative Commons Attribution 4.0 license</span></span></a><span data-key="2b316ea105804e56addff3e8ef7ba753"><span data-offset-key="2b316ea105804e56addff3e8ef7ba753:0">.</span></span></span>

<a href="how-to-read.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42"></a>


<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">How to read this book</span>







<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="index.html#the-book-sites" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">The book sites</span></span>

<a href="index.html#the-author" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">The author</span></span>

<a href="index.html#help" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Help</span></span>

<a href="index.html#helpers" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Helpers</span></span>

<a href="index.html#license" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024"></a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1"><span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">License</span></span>
