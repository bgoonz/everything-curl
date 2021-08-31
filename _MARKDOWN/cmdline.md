<a href="cmdline/options.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Command line options</span>
</a>
<a href="cmdline/versions.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Options depend on version</span>
</a>
<a href="cmdline/urls.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">URLs</span>
</a>
<a href="cmdline/globbing.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">URL globbing</span>
</a>
<a href="cmdline/listopts.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">List options</span>
</a>
<a href="cmdline/configfile.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Config file</span>
</a>
<a href="cmdline/passwords.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Passwords</span>
</a>
<a href="cmdline/progressmeter.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Progress meter</span>
</a>
<a href="bindings.html" class="navButton-94f2579c--navButtonClickable-161b88ca">href="bookindex.html" class="navButton-94f2579c--navButtonClickable-161b88ca">
</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Command line basics</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="3ad657732fe54d5bb77447f93a8087ec">
<span data-offset-key="3ad657732fe54d5bb77447f93a8087ec:0">curl started out as a command-line tool and it has been invoked from shell prompts and from within scripts by thousands of users over the years. curl has established itself as one of those trusty tools that is there for you to help you get your work done.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="c63ab9cc6ea34d45b9818747b7d67c04">
<span data-offset-key="c63ab9cc6ea34d45b9818747b7d67c04:0">Binaries and different platforms</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="6323cb4c14704555903c68253d40b141">
<span data-offset-key="6323cb4c14704555903c68253d40b141:0">The command-line tool "curl" is a binary executable file. The curl project does not by itself distribute or provide binaries. Binary files are highly system specific and oftentimes also bound to specific system versions.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="aff731c91b7c4c43b3fd1d0c6f9b8760">
<span data-offset-key="aff731c91b7c4c43b3fd1d0c6f9b8760:0">To get a curl for your platform and your system, you need to get a curl executable from somewhere. Many people build their own from the source code provided by the curl project, lots of people install it using a package tool for their operating system and yet another portion of users download binary install packages from sources they trust.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="8e46095fc2804fc39837eaf2f53c7436">
<span data-offset-key="8e46095fc2804fc39837eaf2f53c7436:0">No matter how you do it, make sure you are getting your version from a trusted source and that you verify digital signatures or the authenticity of the packages in other ways.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="92ad106ad9ee4c618908b0fa03614385">
<span data-offset-key="92ad106ad9ee4c618908b0fa03614385:0">Also, remember that curl is often built to use third-party libraries to perform and unless curl is built to use them statically you must also have those third-party libraries installed; the exact set of libraries will vary depending on the particular build you get.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="24142293d6dc4ec49f5a56de38eb2115">
<span data-offset-key="24142293d6dc4ec49f5a56de38eb2115:0">Command lines, quotes and aliases</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="0b0faa3bdeb24e4e8613792011c41c98">
<span data-offset-key="0b0faa3bdeb24e4e8613792011c41c98:0">There are many different command lines, shells and prompts in which curl can be used. They all come with their own sets of limitations, rules and guidelines to follow. The curl tool is designed to work with any of them without causing troubles but there may be times when your specific command line system does not match what others use or what is otherwise documented.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="536ac05a7ff146f1a7e8af19e46911fe">
<span data-offset-key="536ac05a7ff146f1a7e8af19e46911fe:0">One way that command-line systems differ, for example, is how you can put quotes around arguments such as to embed spaces or special symbols. In most Unix-like shells you use double quotes (") and single quotes (') depending if you want to allow variable expansions or not within the quoted string, but on Windows there's no support for the single quote version.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="814b609d3d1141458efd34248ab40a84">
<span data-offset-key="814b609d3d1141458efd34248ab40a84:0">In some environments, like PowerShell on Windows, the authors of the command line system decided they know better and "help" the user to use another tool instead of curl when </span>
<span data-offset-key="814b609d3d1141458efd34248ab40a84:1">`curl`</span>
<span data-offset-key="814b609d3d1141458efd34248ab40a84:2"> is typed, by providing an alias that takes precedence when a command line is executed. In order to use curl properly with PowerShell, you need to type in its full name including the extension: "curl.exe".</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="b0bcd63457884f899d88f79aebb2990d">
<span data-offset-key="b0bcd63457884f899d88f79aebb2990d:0">Different command-line environments will also have different maximum command line lengths and force the users to limit how large amount of data that can be put into a single line. curl adapts to this by offering a way to provide command-line options through a file—or from stdin—using the -K option.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="6fd6d510fd7f4cb3b71227b3cdad14a7">
<span data-offset-key="6fd6d510fd7f4cb3b71227b3cdad14a7:0">Garbage in, garbage out</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="850132f8faac47789f1d6bdba3aa6545">
<span data-offset-key="850132f8faac47789f1d6bdba3aa6545:0">curl has little will of its own. It tries to please you and your wishes to a large extent. It also means that it will try to play with what you give it. If you misspell an option, it might do something unintended. If you pass in a slightly illegal URL, chances are curl will still deal with it and proceed. It means that you can pass in crazy data in some options and you can have curl pass on that crazy data in its transfer operation.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="ce537facd55a4abb8d92655bdf46e359">
<span data-offset-key="ce537facd55a4abb8d92655bdf46e359:0">This is a design choice, as it allows you to really tweak how curl does its protocol communications and you can have curl massage your server implementations in the most creative ways.</span>
</span>
</span>
<a href="protocols/curl.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">
</a>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">curl protocols</span>
<a href="cmdline/options.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">
</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Command line options</span>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>
<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>
<a href="cmdline.html#binaries-and-different-platforms" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Binaries and different platforms</span>
</span>
<a href="cmdline.html#command-lines-quotes-and-aliases" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Command lines, quotes and aliases</span>
</span>
<a href="cmdline.html#garbage-in-garbage-out" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Garbage in, garbage out</span>
</span>
