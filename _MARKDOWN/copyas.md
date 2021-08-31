<a href="telnet.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
</a>
<a href="copyas.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">
</a># <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Copy as curl</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="efc38c7fb7364064a049a0d6f71358c8">
<span data-offset-key="efc38c7fb7364064a049a0d6f71358c8:0">Using curl to perform an operation a user just managed to do with his or her browser is one of the more common requests and areas people ask for help about.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="6d3066c19dac4fc9b76a9b78231d1a8f">
<span data-offset-key="6d3066c19dac4fc9b76a9b78231d1a8f:0">How do you get a curl command line to get a resource, just like the browser would get it, nice and easy? Chrome, Firefox and Safari all have this feature.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="e48f57d61c364836a3f107453eabe49a">
<span data-offset-key="e48f57d61c364836a3f107453eabe49a:0">From Firefox</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="9711b852c42c4fe387cb407057f6d04a">
<span data-offset-key="9711b852c42c4fe387cb407057f6d04a:0">You get the site shown with Firefox's network tools. You then right-click on the specific request you want to repeat in the "Web Developer-&gt;Network" tool when you see the HTTP traffic, and in the menu that appears you select "Copy as cURL". Like this screenshot below shows. The operation then generates a curl command line to your clipboard and you can then paste that into your favorite shell window. This feature is available by default in all Firefox installations.</span>
</span>
</span>
<figure>
<img src="https://gblobscdn.gitbook.com/assets%2F-LvW30LMWx5oHe1_SY3L%2F-LvW31Saq-3M0AP13zyD%2F-LvW3J9uORUXhhzbQ921%2Ffirefox-copy-as-curl.png?alt=media" alt="copy as curl with Firefox" class="image-52799b3c" />
<figcaption>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1" style="max-width:100%">copy as curl with Firefox</span>
</figcaption>
</figure>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="d18bb016bef74f7e99afbfdf2e6203c5">
<span data-offset-key="d18bb016bef74f7e99afbfdf2e6203c5:0">From Chrome</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="7309626032d8474182d6e59ff187cb78">
<span data-offset-key="7309626032d8474182d6e59ff187cb78:0">When you pop up the More tools-&gt;Developer mode in Chrome, and you select the Network tab you see the HTTP traffic used to get the resources of the site. On the line of the specific resource you are interested in, you right-click with the mouse and you select "Copy as cURL" and it will generate a command line for you in your clipboard. Paste that in a shell to get a curl command line that makes the transfer. This feature is available by default in all Chrome and Chromium installations.</span>
</span>
</span>
<figure>
<img src="https://gblobscdn.gitbook.com/assets%2F-LvW30LMWx5oHe1_SY3L%2F-LvW31Saq-3M0AP13zyD%2F-LvW3J9wfSCPASN_E9W_%2Fchrome-copy-as-curl.png?alt=media" alt="copy as curl with Chrome" class="image-52799b3c" />
<figcaption>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1" style="max-width:100%">copy as curl with Chrome</span>
</figcaption>
</figure>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="6b2596c17ee5490295db853ecab655a3">
<span data-offset-key="6b2596c17ee5490295db853ecab655a3:0">From Safari</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="60b3fe3ae06144659afc6c26f70db918">
<span data-offset-key="60b3fe3ae06144659afc6c26f70db918:0">In Safari, the "development" menu is not visible until you go into </span>
<span data-offset-key="60b3fe3ae06144659afc6c26f70db918:1">**preferences-&gt;Advanced**</span>
<span data-offset-key="60b3fe3ae06144659afc6c26f70db918:2"> and enable it. But once you have done that, you can select </span>
<span data-offset-key="60b3fe3ae06144659afc6c26f70db918:3">**Show web inspector**</span>
<span data-offset-key="60b3fe3ae06144659afc6c26f70db918:4"> in that development menu and get to see a new console pop up that is similar to the development tools of Firefox and Chrome.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="335770a624464b59b8dd472f6838e1c7">
<span data-offset-key="335770a624464b59b8dd472f6838e1c7:0">Select the network tab, reload the web page and then you can right click the particular resources that you want to fetch with curl, as if you did it with Safari..</span>
</span>
</span>
<figure>
<img src="https://gblobscdn.gitbook.com/assets%2F-LvW30LMWx5oHe1_SY3L%2F-LvW31Saq-3M0AP13zyD%2F-LvW3J9yd3-ri-Zxg1U0%2Fsafari-copy-as-curl.png?alt=media" alt="copy as curl with Safari" class="image-52799b3c" />
<figcaption>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1" style="max-width:100%">copy as curl with Safari</span>
</figcaption>
</figure>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="3d131d4668e847bd8a3d7e51c97967b3">
<span data-offset-key="3d131d4668e847bd8a3d7e51c97967b3:0">On Firefox, without using the devtools</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="f5add24342a044bfadae923c951bb11a">
<span data-offset-key="f5add24342a044bfadae923c951bb11a:0">If this is something you would like to get done more often, you probably find using the developer tools a bit inconvenient and cumbersome to pop up just to get the command line copied. Then </span>
</span>
<a href="https://addons.mozilla.org/en-US/firefox/addon/cliget/" class="link-a079aa82--primary-53a25e66--link-faf6c434">
<span data-key="d0331a7a6086484fb3afc5d7aba527ab">
<span data-offset-key="d0331a7a6086484fb3afc5d7aba527ab:0">cliget</span>
</span>
</a>
<span data-key="6789f59115564a5b85a83773cfa4cec8">
<span data-offset-key="6789f59115564a5b85a83773cfa4cec8:0"> is the perfect add-on for you as it gives you a new option in the right-click menu, so you can get a quick command line generated really quickly, like this example when I right-click an image in Firefox:</span>
</span>
</span>
<figure>
<img src="https://gblobscdn.gitbook.com/assets%2F-LvW30LMWx5oHe1_SY3L%2F-LvW31Saq-3M0AP13zyD%2F-LvW3JA-Ecsj07hat0Hz%2Ffirefox-cliget.png?alt=media" alt="cliget with Firefox" class="image-52799b3c" />
<figcaption>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1" style="max-width:100%">cliget with Firefox</span>
</figcaption>
</figure>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="0636978708f94e52b965c03138f366fa">
<span data-offset-key="0636978708f94e52b965c03138f366fa:0">Not perfect</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="4579caee30a942e591a016a8ba89c27f">
<span data-offset-key="4579caee30a942e591a016a8ba89c27f:0">These methods all give you a command line to reproduce their HTTP transfers. You will also learn they are still often not the perfect solution to your problems. Why? Well mostly because these tools are written to rerun the </span>
<span data-offset-key="4579caee30a942e591a016a8ba89c27f:1">_exact_</span>
<span data-offset-key="4579caee30a942e591a016a8ba89c27f:2"> same request that you copied, while you often want to rerun the same logic but not sending an exact copy of the same cookies and file contents etc.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="85ba0179670143448b25411dccf48ae4">
<span data-offset-key="85ba0179670143448b25411dccf48ae4:0">These tools will give you command lines with static and fixed cookie contents to send in the request, because that is the contents of the cookies that were sent in the browser's requests. You will most likely want to rewrite the command line to dynamically adapt to whatever the content is in the cookie that the server told you in a previous response. And so on.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="2f90042eb57a4c77b57f618dcf3fedf9">
<span data-offset-key="2f90042eb57a4c77b57f618dcf3fedf9:0">The copy as curl functionality is also often notoriously bad at using </span>
<span data-offset-key="2f90042eb57a4c77b57f618dcf3fedf9:1">`-F`</span>
<span data-offset-key="2f90042eb57a4c77b57f618dcf3fedf9:2"> and instead they provide handcrafted </span>
<span data-offset-key="2f90042eb57a4c77b57f618dcf3fedf9:3">`--data-binary`</span>
<span data-offset-key="2f90042eb57a4c77b57f618dcf3fedf9:4"> solutions including the mime separator strings etc.</span>
</span>
</span>
<a href="tls/sslkeylogfile.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">
</a>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">SSLKEYLOGFILE</span>
<a href="../http.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">
</a>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">How to HTTP with curl</span>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 8 months ago</span>
<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>
<a href="copyas.html#from-firefox" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">From Firefox</span>
</span>
<a href="copyas.html#from-chrome" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">From Chrome</span>
</span>
<a href="copyas.html#from-safari" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">From Safari</span>
</span>
<a href="copyas.html#on-firefox-without-using-the-devtools" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">On Firefox, without using the devtools</span>
</span>
<a href="copyas.html#not-perfect" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Not perfect</span>
</span>
