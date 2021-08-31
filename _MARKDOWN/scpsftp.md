<a href="scpsftp.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

</a>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">SCP and SFTP</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="028d5d8e00c84fdcb7705586fc6187cb">

<span data-offset-key="028d5d8e00c84fdcb7705586fc6187cb:0">curl supports the SCP and SFTP protocols if built with the correct prerequisite 3rd party library, </span>

</span>

<a href="https://www.libssh2.org/" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="25ed6febcd5e46679a6910e0be9c2ba6">

<span data-offset-key="25ed6febcd5e46679a6910e0be9c2ba6:0">libssh2</span>

</span>

</a>

<span data-key="305cc93d9a924281b0252127473d08df">

<span data-offset-key="305cc93d9a924281b0252127473d08df:0">.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="918485119c3a4bd5b31a6c93e00adfb5">

<span data-offset-key="918485119c3a4bd5b31a6c93e00adfb5:0">SCP and SFTP are both protocols that are built on top of SSH, a secure and encrypted data protocol that is similar to TLS but differs in a few important ways. For example, SSH does not use certificates of any sort but instead it uses public and private keys. Both SSH and TLS provide strong crypto and secure transfers when used correctly.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b5646bad078d40df9234258c70663a06">

<span data-offset-key="b5646bad078d40df9234258c70663a06:0">The SCP protocol is generally considered to be the black sheep of the two since it is not portable and usually only works between Unix systems.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="86c45b5efefa4be597fbeae654943ab9">

<span data-offset-key="86c45b5efefa4be597fbeae654943ab9:0">URLs</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="293e51cea9374791a5b2302307514bcd">

<span data-offset-key="293e51cea9374791a5b2302307514bcd:0">SFTP and SCP URLs are similar to other URLs and you download files using these protocols the same as with others:</span>

</span>

</span> curl sftp://example.com/file.zip -u user<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ef28dc86c84446038316b7585f8ef7af">

<span data-offset-key="ef28dc86c84446038316b7585f8ef7af:0">and:</span>

</span>

</span> curl scp://example.com/file.zip -u user<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8966ba9d6ce7495ea7027ad39510e137">

<span data-offset-key="8966ba9d6ce7495ea7027ad39510e137:0">SFTP (but not SCP) supports getting a file listing back when the URL ends with a trailing slash:</span>

</span>

</span> curl sftp://example.com/ -u user<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ab45708981874f198cd7845600429f62">

<span data-offset-key="ab45708981874f198cd7845600429f62:0">Note that both these protocols work with "users" and you do not ask for a file anonymously or with a standard generic name. Most systems will require that users authenticate, as outlined below.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="cda44a7792744725928f51afbfce69b3">

<span data-offset-key="cda44a7792744725928f51afbfce69b3:0">When requesting a file from an SFTP or SCP URL, the file path given is considered to be the absolute path on the remote server unless you specifically ask for the path relative to the user's home directory. You do that by making sure the path starts with </span>

<span data-offset-key="cda44a7792744725928f51afbfce69b3:1">`/~/`</span>

<span data-offset-key="cda44a7792744725928f51afbfce69b3:2">. This is quite the opposite to how FTP URLs work and is a common cause for confusion among users.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="abc9dd6ef7f84310b01eb8c5a2911fd7">

<span data-offset-key="abc9dd6ef7f84310b01eb8c5a2911fd7:0">For user </span>

<span data-offset-key="abc9dd6ef7f84310b01eb8c5a2911fd7:1">`daniel`</span>

<span data-offset-key="abc9dd6ef7f84310b01eb8c5a2911fd7:2"> to transfer </span>

<span data-offset-key="abc9dd6ef7f84310b01eb8c5a2911fd7:3">`todo.txt`</span>

<span data-offset-key="abc9dd6ef7f84310b01eb8c5a2911fd7:4"> from his home directory, it would look similar to this:</span>

</span>

</span> curl sftp://example.com/~/todo.txt -u daniel<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="1bb605c77fa34e6eb303f563f1692582">

<span data-offset-key="1bb605c77fa34e6eb303f563f1692582:0">Auth</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2da634ece34445cd9945eaf1104a430d">

<span data-offset-key="2da634ece34445cd9945eaf1104a430d:0">TBD</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="22914b077b7e40c298cc75bda0239cbd">

<span data-offset-key="22914b077b7e40c298cc75bda0239cbd:0">Known hosts</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4707943528564b8db7757dfc8c176e99">

<span data-offset-key="4707943528564b8db7757dfc8c176e99:0">A secure network client needs to make sure that the remote host is exactly the host that it thinks it is communicating with. With TLS based protocols, it is done by the client verifying the server's certificate.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="02e9e893c0324d07a393ed3668d97ddd">

<span data-offset-key="02e9e893c0324d07a393ed3668d97ddd:0">With SSH protocols there are no server certificates, but instead each server can provide its unique key. And unlike TLS, SSH has no certificate authorities or anything so the client simply has to make sure that the host's key matches what it already knows (via other means) it should look like.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="32f0593186bf4b469421a7511f56cee4">

<span data-offset-key="32f0593186bf4b469421a7511f56cee4:0">The matching of keys is typically done using hashes of the key and the file that the client stores the hashes for known servers is often called </span>

<span data-offset-key="32f0593186bf4b469421a7511f56cee4:1">`known_hosts`</span>

<span data-offset-key="32f0593186bf4b469421a7511f56cee4:2"> and is put in a dedicated SSH directory. On Linux systems that is usually called </span>

<span data-offset-key="32f0593186bf4b469421a7511f56cee4:3">`~/.ssh`</span>

<span data-offset-key="32f0593186bf4b469421a7511f56cee4:4">.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="3187593b88004eb99d2c3163f5e78f16">

<span data-offset-key="3187593b88004eb99d2c3163f5e78f16:0">When curl connects to a SFTP and SCP host, it will make sure that the host's key hash is already present in the known hosts file or it will deny continued operation because it cannot trust that the server is the right one. Once the correct hash exists in </span>

<span data-offset-key="3187593b88004eb99d2c3163f5e78f16:1">`known_hosts`</span>

<span data-offset-key="3187593b88004eb99d2c3163f5e78f16:2"> curl can perform transfers.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="925cd709ffe84305bd96c730214024e0">

<span data-offset-key="925cd709ffe84305bd96c730214024e0:0">To force curl to skip checking and obeying to the </span>

<span data-offset-key="925cd709ffe84305bd96c730214024e0:1">`known_hosts`</span>

<span data-offset-key="925cd709ffe84305bd96c730214024e0:2"> file, you can use the </span>

<span data-offset-key="925cd709ffe84305bd96c730214024e0:3">`-k / --insecure`</span>

<span data-offset-key="925cd709ffe84305bd96c730214024e0:4"> command-line option. You must use this option with extreme care since it makes it possible for man-in-the-middle attacks not to be detected.</span>

</span>

</span>

<a href="ftp/advanced.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Advanced FTP use</span>

<a href="reademail.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Reading email</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="scpsftp.html#urls" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">URLs</span>

</span>

<a href="scpsftp.html#auth" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Auth</span>

</span>

<a href="scpsftp.html#known-hosts" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Known hosts</span>

</span>
