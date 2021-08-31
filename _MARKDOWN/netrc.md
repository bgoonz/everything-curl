<a href="netrc.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">
</a>
<a href="telnet.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
</a>
# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">.netrc</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="3009cdcfd4a64830ae996e3fe991450b">
<span data-offset-key="3009cdcfd4a64830ae996e3fe991450b:0">Unix systems have for a long time offered a way for users to store their user name and password for remote FTP servers. ftp clients have supported this for decades and this way allowed users to quickly login to known servers without manually having to reenter the credentials each time. The </span>
<span data-offset-key="3009cdcfd4a64830ae996e3fe991450b:1">`.netrc`</span>
<span data-offset-key="3009cdcfd4a64830ae996e3fe991450b:2"> file is typically stored in a user's home directory. (On Windows, curl will look for it with the name </span>
<span data-offset-key="3009cdcfd4a64830ae996e3fe991450b:3">`_netrc`</span>
<span data-offset-key="3009cdcfd4a64830ae996e3fe991450b:4">).</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="cecbeca41c0145c2ba592c262343a053">
<span data-offset-key="cecbeca41c0145c2ba592c262343a053:0">This being a widespread and well used concept, curl also supports it—if you ask it to. curl does not, however, limit this feature to FTP, but can get credentials for machines for any protocol with this. See further below for how.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="fb7459a4479f445b9174ccde21274ddb">
<span data-offset-key="fb7459a4479f445b9174ccde21274ddb:0">The .netrc file format</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="45f11cb89d2f4e39b1c1e9670c61d45f">
<span data-offset-key="45f11cb89d2f4e39b1c1e9670c61d45f:0">The .netrc file format is simple: you specify lines with a machine name and follow that with lines for the login and password that are associated with that machine.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="553d621a3c2f436b96ec2cd98af745e6">
<span data-offset-key="553d621a3c2f436b96ec2cd98af745e6:0">**machine name**</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="46a6009f4a6a4ce7bd8f87f12d560583">
<span data-offset-key="46a6009f4a6a4ce7bd8f87f12d560583:0">Identifies a remote machine name. curl searches the .netrc file for a machine token that matches the remote machine specified in the URL. Once a match is made, the subsequent .netrc tokens are processed, stopping when the end of file is reached or another machine is encountered.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="ed04964146ba441387e3a57cced58eaf">
<span data-offset-key="ed04964146ba441387e3a57cced58eaf:0">**login name**</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="c43e06383c7b47b09ba5ddbde08e4e01">
<span data-offset-key="c43e06383c7b47b09ba5ddbde08e4e01:0">The user name string for the remote machine.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="a7def81ce67147c8a6b8a8d23501a572">
<span data-offset-key="a7def81ce67147c8a6b8a8d23501a572:0">**password string**</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="7b8c443f92e843948b54c58a267ec814">
<span data-offset-key="7b8c443f92e843948b54c58a267ec814:0">Supply a password. If this token is present, curl will supply the specified string if the remote server requires a password as part of the login process. Note that if this token is present in the .netrc file you really </span>
<span data-offset-key="7b8c443f92e843948b54c58a267ec814:1">**should**</span>
<span data-offset-key="7b8c443f92e843948b54c58a267ec814:2"> make sure the file is not readable by anyone besides the user.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="701ae52b1e0c4c39b58ba6b2429d7e25">
<span data-offset-key="701ae52b1e0c4c39b58ba6b2429d7e25:0">An example .netrc for the host example.com with a user named 'daniel', using the password 'qwerty' would look like:</span>
</span>
</span>    machine example.comlogin danielpassword qwerty<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="3e93d1768ec24258b619d0ad3bc1c599">
<span data-offset-key="3e93d1768ec24258b619d0ad3bc1c599:0">Enable netrc</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="88424bbeb2df47399f4684a7766b696a">
<span data-offset-key="88424bbeb2df47399f4684a7766b696a:0">`-n, --netrc`</span>
<span data-offset-key="88424bbeb2df47399f4684a7766b696a:1"> tells curl to look for and use the .netrc file.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="bb04ace42bdc4ef88018a4f08c720e33">
<span data-offset-key="bb04ace42bdc4ef88018a4f08c720e33:0">`--netrc-file [file]`</span>
<span data-offset-key="bb04ace42bdc4ef88018a4f08c720e33:1"> is similar to </span>
<span data-offset-key="bb04ace42bdc4ef88018a4f08c720e33:2">`--netrc`</span>
<span data-offset-key="bb04ace42bdc4ef88018a4f08c720e33:3">, except that you also provide the path to the actual file to use. This is useful when you want to provide the information in another directory or with another file name.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="86126acf579b438fb398868a20b3772f">
<span data-offset-key="86126acf579b438fb398868a20b3772f:0">`--netrc-optional`</span>
<span data-offset-key="86126acf579b438fb398868a20b3772f:1"> is similar to </span>
<span data-offset-key="86126acf579b438fb398868a20b3772f:2">`--netrc`</span>
<span data-offset-key="86126acf579b438fb398868a20b3772f:3">, but this option makes the .netrc usage optional and not mandatory as the </span>
<span data-offset-key="86126acf579b438fb398868a20b3772f:4">`--netrc`</span>
<span data-offset-key="86126acf579b438fb398868a20b3772f:5"> option.</span>
</span>
</span>
<a href="timeouts.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">
</a>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Timeouts</span>
<a href="proxies.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">
</a>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Proxies</span>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>
<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>
<a href="netrc.html#the-netrc-file-format" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">The .netrc file format</span>
</span>
<a href="netrc.html#enable-netrc" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Enable netrc</span>
</span>
