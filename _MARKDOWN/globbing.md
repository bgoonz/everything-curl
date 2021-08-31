<a href="options.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Command line options</span>

</a>

<a href="versions.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Options depend on version</span>

</a>

<a href="urls.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">URLs</span>

</a>

<a href="globbing.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">URL globbing</span>

</a>

<a href="listopts.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">List options</span>

</a>

<a href="configfile.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Config file</span>

</a>

<a href="passwords.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Passwords</span>

</a>

<a href="progressmeter.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Progress meter</span>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">URL globbing</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4989f73cee9642b8b5056a1e9e55f2bb">

<span data-offset-key="4989f73cee9642b8b5056a1e9e55f2bb:0">At times you want to get a range of URLs that are mostly the same, with only a small portion of it changing between the requests. Maybe it is a numeric range or maybe a set of names. curl offers "globbing" as a way to specify many URLs like that easily.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="55465165286f4271996e85b388561a6c">

<span data-offset-key="55465165286f4271996e85b388561a6c:0">The globbing uses the reserved symbols \[\] and {} for this, symbols that normally cannot be part of a legal URL (except for numerical IPv6 addresses but curl handles them fine anyway). If the globbing gets in your way, disable it with </span>

<span data-offset-key="55465165286f4271996e85b388561a6c:1">`-g, --globoff`</span>

<span data-offset-key="55465165286f4271996e85b388561a6c:2">.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="54bdf47fe35e4ae6a37d0632f5b17bec">

<span data-offset-key="54bdf47fe35e4ae6a37d0632f5b17bec:0">When using \[\] or {} sequences when invoked from a command line prompt, you probably have to put the full URL within double quotes to avoid the shell from interfering with it. This also goes for other characters treated special, like for example '&', '?' and '\*'.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="30a31a48ee1c48208f121cd114358b4e">

<span data-offset-key="30a31a48ee1c48208f121cd114358b4e:0">While most transfer related functionality in curl is provided by the libcurl library, the URL globbing feature is not!</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="c6a27bf680ef477dbbd57759aeb2c62e">

<span data-offset-key="c6a27bf680ef477dbbd57759aeb2c62e:0">Numerical ranges</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="278329543b394db0b2254b2808155278">

<span data-offset-key="278329543b394db0b2254b2808155278:0">You can ask for a numerical range with \[N-M\] syntax, where N is the start index and it goes up to and including M. For example, you can ask for 100 images one by one that are named numerically:</span>

</span>

</span> curl -O "http://example.com/[1-100].png"<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="3ad3067bf65943dc8ce08d1884777d87">

<span data-offset-key="3ad3067bf65943dc8ce08d1884777d87:0">and it can even do the ranges with zero prefixes, like if the number is three digits all the time:</span>

</span>

</span> curl -O "http://example.com/[001-100].png"<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="bb2b5654b24c4e1487b13a5ed767a5d7">

<span data-offset-key="bb2b5654b24c4e1487b13a5ed767a5d7:0">Or maybe you only want even-numbered images so you tell curl a step counter too. This example range goes from 0 to 100 with an increment of 2:</span>

</span>

</span> curl -O "http://example.com/[0-100:2].png"<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="4b5321ea3e274d39a9720a5c89d8bad2">

<span data-offset-key="4b5321ea3e274d39a9720a5c89d8bad2:0">Alphabetical ranges</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a9fe2836bc06496faa8599f38e0026ee">

<span data-offset-key="a9fe2836bc06496faa8599f38e0026ee:0">curl can also do alphabetical ranges, like when a site has sections named a to z:</span>

</span>

</span> curl -O "http://example.com/section[a-z].html"<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="1d00a70b5252439c8d5cb04ca063d892">

<span data-offset-key="1d00a70b5252439c8d5cb04ca063d892:0">A list</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="5e7fd97e2f6347bd9e9c9f0c8453ec7f">

<span data-offset-key="5e7fd97e2f6347bd9e9c9f0c8453ec7f:0">Sometimes the parts do not follow such an easy pattern, and then you can instead give the full list yourself but then within the curly braces instead of the brackets used for the ranges:</span>

</span>

</span> curl -O "http://example.com/{one,two,three,alpha,beta}.html"<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="2330b2c1ecb24dfbbe9709e3140559eb">

<span data-offset-key="2330b2c1ecb24dfbbe9709e3140559eb:0">Combinations</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6fb85d60b25b4f3498577694b242873f">

<span data-offset-key="6fb85d60b25b4f3498577694b242873f:0">You can use several globs in the same URL which then will make curl iterate over those, too. To download the images of Ben, Alice and Frank, in both the resolutions 100 x 100 and 1000 x 1000, a command line could look like:</span>

</span>

</span> curl -O "http://example.com/{Ben,Alice,Frank}-{100x100,1000x1000}.jpg"<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="719aa0e904cb4b40a06baf1fd3ca9248">

<span data-offset-key="719aa0e904cb4b40a06baf1fd3ca9248:0">Or download all the images of a chess board, indexed by two coordinates ranged 0 to 7:</span>

</span>

</span> curl -O "http://example.com/chess-[0-7]x[0-7].jpg"<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7c16cfb985de4d649607119efcfe428d">

<span data-offset-key="7c16cfb985de4d649607119efcfe428d:0">And you can, of course, mix ranges and series. Get a week's worth of logs for both the web server and the mail server:</span>

</span>

</span> curl -O "http://example.com/{web,mail}-log[0-6].txt"<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="c00f95e51b15449589c8e190c9e2dae1">

<span data-offset-key="c00f95e51b15449589c8e190c9e2dae1:0">Output variables for globbing</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="88dc39fa21ba4f00a244c1d74154696d">

<span data-offset-key="88dc39fa21ba4f00a244c1d74154696d:0">In all the globbing examples previously in this chapter we have selected to use the </span>

<span data-offset-key="88dc39fa21ba4f00a244c1d74154696d:1">`-O / --remote-name`</span>

<span data-offset-key="88dc39fa21ba4f00a244c1d74154696d:2"> option, which makes curl save the target file using the file name part of the used URL.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="5f0fbcdf48154969814b029e002acb9b">

<span data-offset-key="5f0fbcdf48154969814b029e002acb9b:0">Sometimes that is not enough. You are downloading multiple files and maybe you want to save them in a different subdirectory or create the saved file names differently. curl, of course, has a solution for these situations as well: output file name variables.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="1ff8c84ffd3d43a1bdae65f1a19bf2db">

<span data-offset-key="1ff8c84ffd3d43a1bdae65f1a19bf2db:0">Each "glob" used in a URL gets a separate variable. They are referenced as '\#\[num\]' - that means the single character '\#' followed by the glob number which starts with 1 for the first glob and ends with the last glob.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7f7eb41291864b019e108b53170e7a3f">

<span data-offset-key="7f7eb41291864b019e108b53170e7a3f:0">Save the main pages of two different sites:</span>

</span>

</span> curl "http://{one,two}.example.com" -o "file\_#1.txt"<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e8676c8dbc6e413983e61a9cb43dc8e1">

<span data-offset-key="e8676c8dbc6e413983e61a9cb43dc8e1:0">Save the outputs from a command line with two globs in a subdirectory:</span>

</span>

</span> curl "http://{site,host}.host[1-5].example.com" -o "subdir/#1\_#2"<a href="urls.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">URLs</span>

<a href="listopts.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">List options</span>

<img src="https://avatars1.githubusercontent.com/u/965580?v=4" class="image-67b14f24--avatar-1c1d03ec" />

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 5 months ago</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="globbing.html#numerical-ranges" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Numerical ranges</span>

</span>

<a href="globbing.html#alphabetical-ranges" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Alphabetical ranges</span>

</span>

<a href="globbing.html#a-list" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">A list</span>

</span>

<a href="globbing.html#combinations" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Combinations</span>

</span>

<a href="globbing.html#output-variables-for-globbing" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Output variables for globbing</span>

</span>
