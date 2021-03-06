<a href="options.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

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

<a href="listopts.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

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

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">List options</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="689cfebe7aa747cf975e27513d80d87f">

<span data-offset-key="689cfebe7aa747cf975e27513d80d87f:0">curl has more than two hundred command-line options and the number of options keep increasing over time. Chances are the number of options will reach 250 within a few years.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8d9489b7b6c64f7ca518722ee443db89">

<span data-offset-key="8d9489b7b6c64f7ca518722ee443db89:0">To find out which options you need to perform as certain action, you can get curl to list them. First, </span>

<span data-offset-key="8d9489b7b6c64f7ca518722ee443db89:1">`curl --help`</span>

<span data-offset-key="8d9489b7b6c64f7ca518722ee443db89:2"> or simply </span>

<span data-offset-key="8d9489b7b6c64f7ca518722ee443db89:3">`curl -h`</span>

<span data-offset-key="8d9489b7b6c64f7ca518722ee443db89:4"> will get you a list of the most important and frequently used options. You can then provide an additional "category" to </span>

<span data-offset-key="8d9489b7b6c64f7ca518722ee443db89:5">`-h`</span>

<span data-offset-key="8d9489b7b6c64f7ca518722ee443db89:6"> to get more options listed for that specific area. Use </span>

<span data-offset-key="8d9489b7b6c64f7ca518722ee443db89:7">`curl -h category`</span>

<span data-offset-key="8d9489b7b6c64f7ca518722ee443db89:8"> to list all existing categories or </span>

<span data-offset-key="8d9489b7b6c64f7ca518722ee443db89:9">`curl -h all`</span>

<span data-offset-key="8d9489b7b6c64f7ca518722ee443db89:10"> to list </span>

<span data-offset-key="8d9489b7b6c64f7ca518722ee443db89:11">_all_</span>

<span data-offset-key="8d9489b7b6c64f7ca518722ee443db89:12"> available options.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7eaeb1898836420b83cf266bad15f456">

<span data-offset-key="7eaeb1898836420b83cf266bad15f456:0">Before curl 7.73.0, the help category system didn't exist and then </span>

<span data-offset-key="7eaeb1898836420b83cf266bad15f456:1">`curl --help`</span>

<span data-offset-key="7eaeb1898836420b83cf266bad15f456:2"> or simply </span>

<span data-offset-key="7eaeb1898836420b83cf266bad15f456:3">`curl -h`</span>

<span data-offset-key="7eaeb1898836420b83cf266bad15f456:4"> would simply list all existing options in alphabetical order with a brief explanation next to each.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f33cf987845f4c729f2ac3f151d2e223">

<span data-offset-key="f33cf987845f4c729f2ac3f151d2e223:0">The </span>

<span data-offset-key="f33cf987845f4c729f2ac3f151d2e223:1">`curl --manual`</span>

<span data-offset-key="f33cf987845f4c729f2ac3f151d2e223:2"> option outputs the entire man page for curl. That is a thorough and complete document on how each option works amassing several thousand lines of documentation. To wade through that is also a tedious work and we encourage use of a search function through those text masses. Some people will appreciate the man page in its </span>

</span>

<a href="https://curl.se/docs/manpage.html" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="a762ee8277764ae6b4ac442d8e631d88">

<span data-offset-key="a762ee8277764ae6b4ac442d8e631d88:0">web version</span>

</span>

</a>

<span data-key="7bea6c5293854a5b861f5ed293a2f42c">

<span data-offset-key="7bea6c5293854a5b861f5ed293a2f42c:0">.</span>

</span>

</span>

<a href="globbing.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">URL globbing</span>

<a href="configfile.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Config file</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 5 months ago</span>
