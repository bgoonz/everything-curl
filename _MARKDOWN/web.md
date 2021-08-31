<a href="layout.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="options.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="style.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="contributing.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="reportvuln.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="web.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Web site</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f735e5c5ee7146e89a6aa48094957a78">

<span data-offset-key="f735e5c5ee7146e89a6aa48094957a78:0">Most of the curl web site is also available in a public git repository, although separate from the source code repository since it generally is not interesting to the same people and we can maintain a different list of people that have push rights, etc.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4a49b52e1aa74e0c923ba33c967e14c4">

<span data-offset-key="4a49b52e1aa74e0c923ba33c967e14c4:0">The web site git repository is available on GitHub at this URL: </span>

</span>

<a href="https://github.com/curl/curl-www" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="9864fd1e28f44750a296e0afdb1a89c5">

<span data-offset-key="9864fd1e28f44750a296e0afdb1a89c5:0">https://github.com/curl/curl-www</span>

</span>

</a>

<span data-key="e2ccdafe9d2741a1a59bff25e0af0e98">

<span data-offset-key="e2ccdafe9d2741a1a59bff25e0af0e98:0"> and you can clone a copy of the web code like this:</span>

</span>

</span> git clone https://github.com/curl/curl-www.git<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="952b6f92943b49aa98a2e312cbb299f2">

<span data-offset-key="952b6f92943b49aa98a2e312cbb299f2:0">Building the web</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="71cbdfd7db864d41a16a62df5dc8e025">

<span data-offset-key="71cbdfd7db864d41a16a62df5dc8e025:0">The web site is a custom-made setup that mostly builds static HTML files from a set of source files. The sources files are preprocessed with what is a souped-up C preprocessor called </span>

</span>

<a href="https://daniel.haxx.se/projects/fcpp/" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="41625f2738a54c6ca4169f8650835688">

<span data-offset-key="41625f2738a54c6ca4169f8650835688:0">fcpp</span>

</span>

</a>

<span data-key="25b2b45925bc419ab2eeacdffe0b6022">

<span data-offset-key="25b2b45925bc419ab2eeacdffe0b6022:0"> and a set of perl scripts. The man pages get converted to HTML with </span>

</span>

<a href="https://daniel.haxx.se/projects/roffit/" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="ee421d65b6a74682b171dfdb3ca6d117">

<span data-offset-key="ee421d65b6a74682b171dfdb3ca6d117:0">roffit</span>

</span>

</a>

<span data-key="dd38e873c0cd4ae9a752b60e397ec116">

<span data-offset-key="dd38e873c0cd4ae9a752b60e397ec116:0">. Make sure fcpp, perl, roffit, make and curl are all in your $PATH.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a99c8098980a43788bb3314d221c71d8">

<span data-offset-key="a99c8098980a43788bb3314d221c71d8:0">Once you have cloned the git repository the first time, invoke </span>

<span data-offset-key="a99c8098980a43788bb3314d221c71d8:1">`sh bootstrap.sh`</span>

<span data-offset-key="a99c8098980a43788bb3314d221c71d8:2"> once to get a symlink and some some initial local files setup, and then you can build the web site locally by invoking </span>

<span data-offset-key="a99c8098980a43788bb3314d221c71d8:3">`make`</span>

<span data-offset-key="a99c8098980a43788bb3314d221c71d8:4"> in the source root tree.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9c8fc514e07446c1b601dd4ff776532d">

<span data-offset-key="9c8fc514e07446c1b601dd4ff776532d:0">Note that this does not make you a complete web site mirror, as some scripts and files are only available on the real actual site, but should give you enough to let you view most HTML pages locally.</span>

</span>

</span>

<a href="reportvuln.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Reporting vulnerabilities</span>

<a href="build.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Build and install</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 12 months ago</span>
