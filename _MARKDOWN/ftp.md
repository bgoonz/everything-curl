<a href="ftp/twoconnections.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Two connections</span>
</a>
<a href="ftp/traversedir.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Directory traversing</span>
</a>
<a href="ftp/advanced.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Advanced FTP use</span>
</a>
<a href="telnet.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
</a>
# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">FTP</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="1e970a7774c744599957fea37fa99109">
<span data-offset-key="1e970a7774c744599957fea37fa99109:0">FTP, the File Transfer Protocol, is probably the oldest network protocol that curl supports—it was created in the early 1970s. The official spec that still is the go-to documentation is </span>
</span>
<a href="https://www.ietf.org/rfc/rfc959.txt" class="link-a079aa82--primary-53a25e66--link-faf6c434">
<span data-key="4f6848a562fe456aad979a49c70c491f">
<span data-offset-key="4f6848a562fe456aad979a49c70c491f:0">RFC 959</span>
</span>
</a>
<span data-key="7c295228f447475eaebef272e9e899b8">
<span data-offset-key="7c295228f447475eaebef272e9e899b8:0">, from 1985, published well over a decade before the first curl release.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="afd9a2f479374b99940b57ca7dd8f7e4">
<span data-offset-key="afd9a2f479374b99940b57ca7dd8f7e4:0">FTP was created in a different era of the Internet and computers and as such it works a little bit differently than most other protocols. These differences can often be ignored and things will just work, but they are also important to know at times when things do not run as planned.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="d8bd0a1341ab4a37bc24e5614dc2799c">
<span data-offset-key="d8bd0a1341ab4a37bc24e5614dc2799c:0">Ping-pong</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="971765b6dcdb4ab987dd9be2a3cb4ef4">
<span data-offset-key="971765b6dcdb4ab987dd9be2a3cb4ef4:0">The FTP protocol is a command and response protocol; the client sends a command and the server responds. If you use curl's </span>
<span data-offset-key="971765b6dcdb4ab987dd9be2a3cb4ef4:1">`-v`</span>
<span data-offset-key="971765b6dcdb4ab987dd9be2a3cb4ef4:2"> option you will get to see all the commands and responses during a transfer.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="689b5634648e48fa9dad055c3efbf56f">
<span data-offset-key="689b5634648e48fa9dad055c3efbf56f:0">For an ordinary transfer, there are something like 5 to 8 commands necessary to send and as many responses to wait for and read. Perhaps needlessly to say, if the server is in a remote location there will be a lot of time waiting for the ping pong to go through before the actual file transfer can be set up and get started. For small files, the initial commands can take longer time than the actual data transfer.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="c44d475e3bfb4fb5a75bbe66a61bc06d">
<span data-offset-key="c44d475e3bfb4fb5a75bbe66a61bc06d:0">Transfer mode</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="6166b20edf7e4ad29237e688753c3356">
<span data-offset-key="6166b20edf7e4ad29237e688753c3356:0">When an FTP client is about to transfer data, it specifies to the server which "transfer mode" it would like the upcoming transfer to use. The two transfer modes curl supports are 'ASCII' and 'BINARY'. Ascii is for text and usually means that the server will send the files with converted newlines while binary means sending the data unaltered and assuming the file is not text.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="b4f5bd85428b484e800b3968c8abaa69">
<span data-offset-key="b4f5bd85428b484e800b3968c8abaa69:0">curl will default to binary transfer mode for FTP, and you ask for ascii mode instead with </span>
<span data-offset-key="b4f5bd85428b484e800b3968c8abaa69:1">`-B, --use-ascii`</span>
<span data-offset-key="b4f5bd85428b484e800b3968c8abaa69:2"> or by making sure the URL ends with </span>
<span data-offset-key="b4f5bd85428b484e800b3968c8abaa69:3">`;type=A`</span>
<span data-offset-key="b4f5bd85428b484e800b3968c8abaa69:4">.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="5598fb71bd5a4daab539079d57859f47">
<span data-offset-key="5598fb71bd5a4daab539079d57859f47:0">Authentication</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="528bffab9b8a434993ae8301fbb154a7">
<span data-offset-key="528bffab9b8a434993ae8301fbb154a7:0">FTP is one of the protocols you normally do not access without a user name and password. It just happens that for systems that allow "anonymous" FTP access you can login with pretty much any name and password you like. When curl is used on an FTP URL to do transfer without any given user name or password, it uses the name </span>
<span data-offset-key="528bffab9b8a434993ae8301fbb154a7:1">`anonymous`</span>
<span data-offset-key="528bffab9b8a434993ae8301fbb154a7:2"> with the password </span>
<span data-offset-key="528bffab9b8a434993ae8301fbb154a7:3">`[email protected]`</span>
<span data-offset-key="528bffab9b8a434993ae8301fbb154a7:4">.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="f2e4b466ce454361b936e3c5cecb655e">
<span data-offset-key="f2e4b466ce454361b936e3c5cecb655e:0">If you want to provide another user name and password, you can pass them on to curl either with the </span>
<span data-offset-key="f2e4b466ce454361b936e3c5cecb655e:1">`-u, --user`</span>
<span data-offset-key="f2e4b466ce454361b936e3c5cecb655e:2"> option or embed the info in the URL:</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="c5561bc788bb42b28eff928a8662d8d2">
<span data-offset-key="c5561bc788bb42b28eff928a8662d8d2:0">curl --user daniel:secret ftp://example.com/download</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="c5092278b813484ea49764a145bf3687">
<span data-offset-key="c5092278b813484ea49764a145bf3687:0">curl ftp://daniel:<a href="../cdn-cgi/l/email-protection.html" class="__cf_email__">[email protected]</a>/download</span>
</span>
</span>
<a href="returns.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">
</a>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Exit status</span>
<a href="ftp/twoconnections.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">
</a>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Two connections</span>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 12 months ago</span>
<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>
<a href="ftp.html#ping-pong" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Ping-pong</span>
</span>
<a href="ftp.html#transfer-mode" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Transfer mode</span>
</span>
<a href="ftp.html#authentication" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Authentication</span>
</span>
