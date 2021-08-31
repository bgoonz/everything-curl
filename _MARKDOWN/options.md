<a href="options.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Command line options</span>
</a>
<a href="versions.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Options depend on version</span>
</a>
<a href="urls.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">URLs</span>
</a>
<a href="globbing.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
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
</a># <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Command line options</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="6889b47104b74d07a5d7353d30fbed4d">
<span data-offset-key="6889b47104b74d07a5d7353d30fbed4d:0">When telling curl to do something, you invoke curl with zero, one or several command-line options to accompany the URL or set of URLs you want the transfer to be about. curl supports over two hundred different options.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="caaa0b3edb114d1f845a1febd97f0061">
<span data-offset-key="caaa0b3edb114d1f845a1febd97f0061:0">Short options</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="299e4c0d84ea45fe8f23527dffd690b0">
<span data-offset-key="299e4c0d84ea45fe8f23527dffd690b0:0">Command line options pass on information to curl about how you want it to behave. Like you can ask curl to switch on verbose mode with the -v option:</span>
</span>
</span>    curl -v http://example.com<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="92fafc02aa6943f399ec8bc2798cfc9f">
<span data-offset-key="92fafc02aa6943f399ec8bc2798cfc9f:0">-v is here used as a "short option". You write those with the minus symbol and a single letter immediately following it. Many options are just switches that switch something on or change something between two known states. They can be used with just that option name. You can then also combine several single-letter options after the minus. To ask for both verbose mode and that curl follows HTTP redirects:</span>
</span>
</span>    curl -vL http://example.com<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="7dc8cf26bb534a68b43d35aaca0eeade">
<span data-offset-key="7dc8cf26bb534a68b43d35aaca0eeade:0">The command-line parser in curl always parses the entire line and you can put the options anywhere you like; they can also appear after the URL:</span>
</span>
</span>    curl http://example.com -Lv<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="a7d3540d112947f7a8f5056832f1056e">
<span data-offset-key="a7d3540d112947f7a8f5056832f1056e:0">and the two separate short options can of course also be specified separately, like:</span>
</span>
</span>    curl -v -L http://example.com<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="56174cca91d04b45a44030e443e21474">
<span data-offset-key="56174cca91d04b45a44030e443e21474:0">Long options</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="69c8e6d48e1d4197af8fd979170ecd06">
<span data-offset-key="69c8e6d48e1d4197af8fd979170ecd06:0">Single-letter options are convenient since they are quick to write and use, but as there are only a limited number of letters in the alphabet and there are many things to control, not all options are available like that. Long option names are therefore provided for those. Also, as a convenience and to allow scripts to become more readable, most short options have longer name aliases.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="61fe644b7c9849e8810b39bb712b0717">
<span data-offset-key="61fe644b7c9849e8810b39bb712b0717:0">Long options are always written with </span>
<span data-offset-key="61fe644b7c9849e8810b39bb712b0717:1">_two_</span>
<span data-offset-key="61fe644b7c9849e8810b39bb712b0717:2"> minuses (or </span>
<span data-offset-key="61fe644b7c9849e8810b39bb712b0717:3">_dashes_</span>
<span data-offset-key="61fe644b7c9849e8810b39bb712b0717:4">, whichever you prefer to call them) and then the name and you can only write one option name per double-minus. Asking for verbose mode using the long option format looks like:</span>
</span>
</span>    curl --verbose http://example.com<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="7baf63549f2748bb8f8de854e3d1154f">
<span data-offset-key="7baf63549f2748bb8f8de854e3d1154f:0">and asking for HTTP redirects as well using the long format looks like:</span>
</span>
</span>    curl --verbose --location http://example.com<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="aedf3da1200140198027da9c7cf8bb1d">
<span data-offset-key="aedf3da1200140198027da9c7cf8bb1d:0">Arguments to options</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="c09bf76f12a74b08b0e079b0d0f093ba">
<span data-offset-key="c09bf76f12a74b08b0e079b0d0f093ba:0">Not all options are just simple boolean flags that enable or disable features. For some of them you need to pass on data, like perhaps a user name or a path to a file. You do this by writing first the option and then the argument, separated with a space. Like, for example, if you want to send an arbitrary string of data in an HTTP POST to a server:</span>
</span>
</span>    curl -d arbitrary http://example.com<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="d7133109d14d4908b8ad98654f5c5f29">
<span data-offset-key="d7133109d14d4908b8ad98654f5c5f29:0">and it works the same way even if you use the long form of the option:</span>
</span>
</span>    curl --data arbitrary http://example.com<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="56b05c47b93a4224a5953b77cd9090f5">
<span data-offset-key="56b05c47b93a4224a5953b77cd9090f5:0">When you use the short options with arguments, you can, in fact, also write the data without the space separator:</span>
</span>
</span>    curl -darbitrary http://example.com<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="35eaf0c0369f4b99aeb2aaa8f1a3e9b8">
<span data-offset-key="35eaf0c0369f4b99aeb2aaa8f1a3e9b8:0">Arguments with spaces</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="6bf276944bb54f66882845c95b47651f">
<span data-offset-key="6bf276944bb54f66882845c95b47651f:0">At times you want to pass on an argument to an option, and that argument contains one or more spaces. For example you want to set the user-agent field curl uses to be exactly </span>
<span data-offset-key="6bf276944bb54f66882845c95b47651f:1">`I am your father`</span>
<span data-offset-key="6bf276944bb54f66882845c95b47651f:2">, including those three spaces. Then you need to put quotes around the string when you pass it to curl on the command line. The exact quotes to use varies depending on your shell/command prompt, but generally it will work with double quotes in most places:</span>
</span>
</span>    curl -A "I am your father" http://example.com<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="043d58a9ce444228b158946fddc8fadf">
<span data-offset-key="043d58a9ce444228b158946fddc8fadf:0">Failing to use quotes, like if you would write the command line like this:</span>
</span>
</span>    curl -A I am your father http://example.com<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="56e91ff5b20c4e06ba51965a7789cf83">
<span data-offset-key="56e91ff5b20c4e06ba51965a7789cf83:0">… will make curl only use 'I' as a user-agent string, and the following strings, 'am', your, etc will instead all be treated as separate URLs since they do not start with </span>
<span data-offset-key="56e91ff5b20c4e06ba51965a7789cf83:1">`-`</span>
<span data-offset-key="56e91ff5b20c4e06ba51965a7789cf83:2"> to indicate that they are options and curl only ever handles options and URLs.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="d4a2cded317d41c383bfc4f819ef0468">
<span data-offset-key="d4a2cded317d41c383bfc4f819ef0468:0">To make the string itself contain double quotes, which is common when you for example want to send a string of JSON to the server, you may need to use single quotes (except on Windows, where single quotes does not work the same way). Send the JSON string </span>
<span data-offset-key="d4a2cded317d41c383bfc4f819ef0468:1">`{ "name": "Darth" }`</span>
<span data-offset-key="d4a2cded317d41c383bfc4f819ef0468:2">:</span>
</span>
</span>    curl -d '{ "name": "Darth" }' http://example.com<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="39102e31e65842b2b3a4395db38817e4">
<span data-offset-key="39102e31e65842b2b3a4395db38817e4:0">Or if you want to avoid the single quote thing, you may prefer to send the data to curl via a file, which then does not need the extra quoting. Assuming we call the file 'json' that contains the above mentioned data:</span>
</span>
</span>    curl -d @json http://example.com<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="6f8cf025c931454f917b05fde57f41dc">
<span data-offset-key="6f8cf025c931454f917b05fde57f41dc:0">Negative options</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="33cd62a85af442a887f7563ccc8e340c">
<span data-offset-key="33cd62a85af442a887f7563ccc8e340c:0">For options that switch on something, there is also a way to switch it off. You then use the long form of the option with an initial </span>
<span data-offset-key="33cd62a85af442a887f7563ccc8e340c:1">`no-`</span>
<span data-offset-key="33cd62a85af442a887f7563ccc8e340c:2"> prefix before the name. As an example, to switch off verbose mode:</span>
</span>
</span>    curl --no-verbose http://example.com<a href="../cmdline.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">
</a>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Command line basics</span>
<a href="versions.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">
</a>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Options depend on version</span>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 5 months ago</span>
<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>
<a href="options.html#short-options" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Short options</span>
</span>
<a href="options.html#long-options" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Long options</span>
</span>
<a href="options.html#arguments-to-options" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Arguments to options</span>
</span>
<a href="options.html#arguments-with-spaces" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Arguments with spaces</span>
</span>
<a href="options.html#negative-options" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Negative options</span>
</span>
