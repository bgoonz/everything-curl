<a href="../version.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="../persist.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="../telnet.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

<a href="sslkeylogfile.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">SSLKEYLOGFILE</span>

</a>

<a href="../copyas.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">SSLKEYLOGFILE</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<figure>

<img src="https://gblobscdn.gitbook.com/assets%2F-LvW30LMWx5oHe1_SY3L%2F-LvW31Saq-3M0AP13zyD%2F-LvW3KJpv_aPnmobSWEB%2Fwireshark-screenshot.png?alt=media" alt="view network traffic with wireshark" class="image-52799b3c" />

<figcaption>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1" style="max-width:100%">view network traffic with wireshark</span>

</figcaption>

</figure>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="15dd344b32104aed93a856bb667cb43d">

<span data-offset-key="15dd344b32104aed93a856bb667cb43d:0">Since a long time back, the venerable network analyzer tool Wireshark (screenshot above) has provided a way to decrypt and inspect TLS traffic when sent and received by Firefox and Chrome.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b27bdd095b7c4829a42c5ef0baece056">

<span data-offset-key="b27bdd095b7c4829a42c5ef0baece056:0">This is similarly possible to do with curl.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0d9546fa708f436ab5743f60d92689ca">

<span data-offset-key="0d9546fa708f436ab5743f60d92689ca:0">You do this by making the browser or curl tell Wireshark the SSL secrets so that it can decrypt them:</span>

</span>

</span>

1.  <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
    <span data-key="19bc93bdb8fa497c9d8d5847ac9f2257">
    <span data-offset-key="19bc93bdb8fa497c9d8d5847ac9f2257:0">set the environment variable named </span>
    <span data-offset-key="19bc93bdb8fa497c9d8d5847ac9f2257:1">`SSLKEYLOGFILE`</span>
    <span data-offset-key="19bc93bdb8fa497c9d8d5847ac9f2257:2"> to a file name of your choice before you start the browser or curl</span>
    </span>
    </span>

2.  <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
    <span data-key="8b5bb02b05e2401a8230c5dce7903c7d">
    <span data-offset-key="8b5bb02b05e2401a8230c5dce7903c7d:0">Setting the same file name path in the Master-secret field in Wireshark. Go to Preferences-&gt;Protocols-&gt;TLS (SSL in older versions) and edit the path as shown in the screenshot below.</span>
    </span>
    </span>

<figure>

<img src="https://gblobscdn.gitbook.com/assets%2F-LvW30LMWx5oHe1_SY3L%2F-LvW31Saq-3M0AP13zyD%2F-LvW3KJrfDmSVhybPZdn%2Fwireshark-ssl-master-secret.png?alt=media" alt="set the ssl key file name" class="image-52799b3c" />

<figcaption>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1" style="max-width:100%">set the ssl key file name</span>

</figcaption>

</figure>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0b2387d3540f40908683f093b789b800">

<span data-offset-key="0b2387d3540f40908683f093b789b800:0">Having done this simple operation, you can now inspect curl's or your browser's HTTPS traffic in Wireshark. Just super handy and awesome.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ed23566ea999444cb9e2baddfcd3d991">

<span data-offset-key="ed23566ea999444cb9e2baddfcd3d991:0">Just remember that if you record TLS traffic and want to save it for analyzing later, you need to also save the file with the secrets so that you can decrypt that traffic capture at a later time as well.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="0701af4408b146009a7be24ad7e4fbf6">

<span data-offset-key="0701af4408b146009a7be24ad7e4fbf6:0">libcurl-using applications too!</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="741ac220d96f4fb7a2a291e428df7847">

<span data-offset-key="741ac220d96f4fb7a2a291e428df7847:0">Support for </span>

<span data-offset-key="741ac220d96f4fb7a2a291e428df7847:1">`SSLKEYLOGFILE`</span>

<span data-offset-key="741ac220d96f4fb7a2a291e428df7847:2"> is provided by libcurl itself - making it possible for you to trace and inspect the TLS network data for any application built to use libcurl - not just the curl command line tool.</span>

</span>

</span>

<a href="../tls.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">TLS</span>

<a href="../copyas.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Copy as curl</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 1 year ago</span>
