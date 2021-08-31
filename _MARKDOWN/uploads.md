<a href="uploads.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

</a>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Uploads</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0a12a3814dd74269a2b84e3eec801c13">

<span data-offset-key="0a12a3814dd74269a2b84e3eec801c13:0">Uploading is a term for sending data to a remote server. Uploading is done differently for each protocol, and several protocols may even allow different ways of uploading data.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="05a025871a65499699df76979949776f">

<span data-offset-key="05a025871a65499699df76979949776f:0">Protocols allowing upload</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="70cbb30bf98d4e688945feee8cc48a59">

<span data-offset-key="70cbb30bf98d4e688945feee8cc48a59:0">You can upload data using one of these protocols: FILE, FTP, FTPS, HTTP, HTTPS, IMAP, IMAPS, SCP, SFTP, SMB, SMBS, SMTP, SMTPS and TFTP.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="12d4f3de9590489bbd0931cb5bf63bde">

<span data-offset-key="12d4f3de9590489bbd0931cb5bf63bde:0">HTTP offers several "uploads"</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="fb730e2dadd04c4285d875ea306bd516">

<span data-offset-key="fb730e2dadd04c4285d875ea306bd516:0">HTTP (and its bigger brother HTTPS) provides several different ways to upload data to a server and curl offers easy command-line options to do it the three most common ways, described below.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e0ede6c11b8043c78f2e0fd64906eec1">

<span data-offset-key="e0ede6c11b8043c78f2e0fd64906eec1:0">An interesting detail with HTTP is also that an upload can also be a download, in the same operation and in fact many downloads are initiated with an HTTP POST.</span>

</span>

</span>

<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="a740cb1576334e22b683c43cc665a7b5">

<span data-offset-key="a740cb1576334e22b683c43cc665a7b5:0">POST</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="688ea7e18ec646b7afc4e760c645abf9">

<span data-offset-key="688ea7e18ec646b7afc4e760c645abf9:0">POST is the HTTP method that was invented to send data to a receiving web application, and it is, for example, how most common HTML forms on the web work. It usually sends a chunk of relatively small amounts of data to the receiver.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="3bc7d82c196540c1bdb12ba955ec9fe2">

<span data-offset-key="3bc7d82c196540c1bdb12ba955ec9fe2:0">The upload kind is usually done with the </span>

<span data-offset-key="3bc7d82c196540c1bdb12ba955ec9fe2:1">`-d`</span>

<span data-offset-key="3bc7d82c196540c1bdb12ba955ec9fe2:2"> or </span>

<span data-offset-key="3bc7d82c196540c1bdb12ba955ec9fe2:3">`--data`</span>

<span data-offset-key="3bc7d82c196540c1bdb12ba955ec9fe2:4"> options, but there are a few additional alterations.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="d477cec713384b2daa8150c665f1fba3">

<span data-offset-key="d477cec713384b2daa8150c665f1fba3:0">Read the detailed description on how to do this with curl in the </span>

</span>

<a href="../http/post.html" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="2e55939b3a294a08b04867b8bceb4bac">

<span data-offset-key="2e55939b3a294a08b04867b8bceb4bac:0">HTTP POST with curl</span>

</span>

</a>

<span data-key="7e6fc21e0a3b447cb895d2466c025f71">

<span data-offset-key="7e6fc21e0a3b447cb895d2466c025f71:0"> chapter.</span>

</span>

</span>

<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="3162c484291d4783b1aaaeb8d7ad0211">

<span data-offset-key="3162c484291d4783b1aaaeb8d7ad0211:0">multipart formpost</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="35b3623408c74fd1803deef8f5960d86">

<span data-offset-key="35b3623408c74fd1803deef8f5960d86:0">Multipart formposts are also used in HTML forms on web sites; typically when there's a file upload involved. This type of upload is also an HTTP POST but it sends the data formatted according to some special rules, which is what the "multipart" name means.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="57f037abd0b24b7b9b45f7b7ba138474">

<span data-offset-key="57f037abd0b24b7b9b45f7b7ba138474:0">Since it sends the data formatted completely differently, you cannot select which type of POST to use at your own whim but it entirely depends on what the receiving server end expects and can handle.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="5fb0f8ea955e46c98c27518bb90ffa72">

<span data-offset-key="5fb0f8ea955e46c98c27518bb90ffa72:0">HTTP multipart formposts are done with </span>

<span data-offset-key="5fb0f8ea955e46c98c27518bb90ffa72:1">`-F`</span>

<span data-offset-key="5fb0f8ea955e46c98c27518bb90ffa72:2">. See the detailed description in the </span>

</span>

<a href="../http/multipart.html" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="4f96f7f292ce48cbacbbbff9c6a0e3c9">

<span data-offset-key="4f96f7f292ce48cbacbbbff9c6a0e3c9:0">HTTP multipart formposts</span>

</span>

</a>

<span data-key="c8ce47da77d84a15a91e2bd1e0d73a4d">

<span data-offset-key="c8ce47da77d84a15a91e2bd1e0d73a4d:0"> chapter.</span>

</span>

</span>

<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">

<span data-key="d6d0382a40cc4108b8909adc2b763790">

<span data-offset-key="d6d0382a40cc4108b8909adc2b763790:0">PUT</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b06fa5fc41da493fbd8fb896545bbc90">

<span data-offset-key="b06fa5fc41da493fbd8fb896545bbc90:0">HTTP PUT is the upload method that was designed to send a complete resource meant to be put as-is on the remote site or even replace an existing resource there. That said, this is also the least used upload method for HTTP on the web today and lots, if not most, web servers do not even have PUT enabled.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="42009ca0c4154bebbf8f093b6320598e">

<span data-offset-key="42009ca0c4154bebbf8f093b6320598e:0">You send off an HTTP upload using the -T option with the file to upload:</span>

</span>

</span>    curl -T uploadthis http://example.com/<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="521189dcfa23475b895ec0cc021e7f6a">

<span data-offset-key="521189dcfa23475b895ec0cc021e7f6a:0">FTP uploads</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="88ad7d6ce1004bcfb64b1881033d4f95">

<span data-offset-key="88ad7d6ce1004bcfb64b1881033d4f95:0">Working with FTP, you get to see the remote file system you will be accessing. You tell the server exactly in which directory you want the upload to be placed and which file name to use. If you specify the upload URL with a trailing slash, curl will append the locally used file name to the URL and then that will be the file name used when stored remotely:</span>

</span>

</span>    curl -T uploadthis ftp://example.com/this/directory/<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="486b189feb3b4e3884b2d1c95ce077d8">

<span data-offset-key="486b189feb3b4e3884b2d1c95ce077d8:0">So if you prefer to select a different file name on the remote side than what you have used locally, you specify it in the URL:</span>

</span>

</span>    curl -T uploadthis ftp://example.com/this/directory/remotename<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8c58e99800b04ad68de6fef9bde1f169">

<span data-offset-key="8c58e99800b04ad68de6fef9bde1f169:0">Learn more about FTPing with curl in the </span>

</span>

<a href="ftp.html" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="8fb35f4e3d6e4f22aabc450a417744a0">

<span data-offset-key="8fb35f4e3d6e4f22aabc450a417744a0:0">Using curl/FTP</span>

</span>

</a>

<span data-key="fe4f2c19c76b4ddfa5cd55fcfd8520f1">

<span data-offset-key="fe4f2c19c76b4ddfa5cd55fcfd8520f1:0"> section.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="9440fca3118f4391b28cede7d96e6790">

<span data-offset-key="9440fca3118f4391b28cede7d96e6790:0">SMTP uploads</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="17e5f44b6b974e28af6213f64a7d31b6">

<span data-offset-key="17e5f44b6b974e28af6213f64a7d31b6:0">You may not consider sending an e-mail to be "uploading", but to curl it is. You upload the mail body to the SMTP server. With SMTP, you also need to include all the e-mail headers you need (To:, From:, Date:, etc.) in the mail body as curl will not add any at all.</span>

</span>

</span>    curl -T mail smtp://mail.example.com/ --mail-from [email protected]<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b0daee0ce9fe40a78a499f082ac11570">

<span data-offset-key="b0daee0ce9fe40a78a499f082ac11570:0">Learn more about using SMTP with curl in the </span>

</span>

<a href="smtp.html" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="8b64fc60d73d43c19990016d10410d0d">

<span data-offset-key="8b64fc60d73d43c19990016d10410d0d:0">Using curl/SMTP</span>

</span>

</a>

<span data-key="a22ae17920384ca4863a43ed9804b329">

<span data-offset-key="a22ae17920384ca4863a43ed9804b329:0"> section.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="76209a15604f4348a12ebd27c2d42889">

<span data-offset-key="76209a15604f4348a12ebd27c2d42889:0">Progress meter for uploads</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8c2fab871a8a4f09b9032f60a41eb47f">

<span data-offset-key="8c2fab871a8a4f09b9032f60a41eb47f:0">The general progress meter curl provides (see the </span>

</span>

<a href="../cmdline/progressmeter.html" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="8e18b7c20ae8470a94f685ec5d63f005">

<span data-offset-key="8e18b7c20ae8470a94f685ec5d63f005:0">Progress meter</span>

</span>

</a>

<span data-key="3276d2cba0a44ad6938b634b9d72f724">

<span data-offset-key="3276d2cba0a44ad6938b634b9d72f724:0"> section) works fine for uploads as well. What needs to be remembered is that the progress meter is automatically disabled when you are sending output to stdout, and most protocols curl support can output something even for an upload.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="679fd8a8b4ed458e978d8534b66d455f">

<span data-offset-key="679fd8a8b4ed458e978d8534b66d455f:0">Therefore, you may need to explicitly redirect the downloaded data to a file (using shell redirect '&gt;', </span>

<span data-offset-key="679fd8a8b4ed458e978d8534b66d455f:1">`-o`</span>

<span data-offset-key="679fd8a8b4ed458e978d8534b66d455f:2"> or similar) to get the progress meter displayed for upload.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="5d107987b16e4005887d59bc68c3d266">

<span data-offset-key="5d107987b16e4005887d59bc68c3d266:0">Rate limiting</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4baa9cd45aa1424090601f8dba4e7f99">

<span data-offset-key="4baa9cd45aa1424090601f8dba4e7f99:0">Rate limiting works exactly the same for uploads as for downloads and curl, in fact, only has a single limit that will limit the speed in both directions.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b959833f79b34bf7ae53e2f17e005f2c">

<span data-offset-key="b959833f79b34bf7ae53e2f17e005f2c:0">See further details in the </span>

</span>

<a href="downloads.html#rate-limiting" class="link-a079aa82--primary-53a25e66--link-faf6c434">

<span data-key="fdef49eab9a1426fad3a7967542be4de">

<span data-offset-key="fdef49eab9a1426fad3a7967542be4de:0">Download Rate limiting section</span>

</span>

</a>

<span data-key="9022cbb890034248bca2487b68e22fc7">

<span data-offset-key="9022cbb890034248bca2487b68e22fc7:0">.</span>

</span>

</span>

<a href="downloads.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Downloads</span>

<a href="connections.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Connections</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 8 months ago</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="uploads.html#protocols-allowing-upload" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Protocols allowing upload</span>

</span>

<a href="uploads.html#http-offers-several-uploads" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">HTTP offers several "uploads"</span>

</span>

<a href="uploads.html#post" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">POST</span>

</span>

<a href="uploads.html#multipart-formpost" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">multipart formpost</span>

</span>

<a href="uploads.html#put" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">PUT</span>

</span>

<a href="uploads.html#ftp-uploads" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">FTP uploads</span>

</span>

<a href="uploads.html#smtp-uploads" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">SMTP uploads</span>

</span>

<a href="uploads.html#progress-meter-for-uploads" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Progress meter for uploads</span>

</span>

<a href="uploads.html#rate-limiting" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Rate limiting</span>

</span>
