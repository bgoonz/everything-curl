<a href="verbose/trace.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Trace options</span>
</a>
<a href="verbose/writeout.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Write out</span>
</a>
<a href="telnet.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
</a>
# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Verbose</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="7b12661d0d2e4daeb99e931d2085ddf5">
<span data-offset-key="7b12661d0d2e4daeb99e931d2085ddf5:0">If your curl command does not execute or return what you expected it to, your first gut reaction should always be to run the command with the </span>
<span data-offset-key="7b12661d0d2e4daeb99e931d2085ddf5:1">`-v / --verbose`</span>
<span data-offset-key="7b12661d0d2e4daeb99e931d2085ddf5:2"> option to get more information.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="fff131e4e6ef4200af9ad7f28fe6228c">
<span data-offset-key="fff131e4e6ef4200af9ad7f28fe6228c:0">When verbose mode is enabled, curl gets more talkative and will explain and show a lot more of its doings. It will add informational tests and prefix them with '\*'. For example, let's see what curl might say when trying a simple HTTP example (saving the downloaded data in the file called 'saved'):</span>
</span>
</span>    $ curl -v http://example.com -o saved* Rebuilt URL to: http://example.com/<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="fc28095d02484cbb9265442690c527f5">
<span data-offset-key="fc28095d02484cbb9265442690c527f5:0">Ok so we invoked curl with a URL that it considers incomplete so it helps us and it adds a trailing slash before it moves on.</span>
</span>
</span>        *   Trying 93.184.216.34...<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="c56a047ab88c4b61adcbec97b43412a0">
<span data-offset-key="c56a047ab88c4b61adcbec97b43412a0:0">This tells us curl now tries to connect to this IP address. It means the name 'example.com' has been resolved to one or more addresses and this is the first (and possibly only) address curl will try to connect to.</span>
</span>
</span>        * Connected to example.com (93.184.216.34) port 80 (#0)<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="d744288b658a4f68aff8002c5717af3c">
<span data-offset-key="d744288b658a4f68aff8002c5717af3c:0">It worked! curl connected to the site and here it explains how the name maps to the IP address and on which port it has connected to. The '(\#0)' part is which internal number curl has given this connection. If you try multiple URLs in the same command line you can see it use more connections or reuse connections, so the connection counter may increase or not increase depending on what curl decides it needs to do.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="ed0a349ed21b46ce85aa29458caa4382">
<span data-offset-key="ed0a349ed21b46ce85aa29458caa4382:0">If we use an HTTPS:// URL instead of an HTTP one, there will also be a whole bunch of lines explaining how curl uses CA certs to verify the server's certificate and some details from the server's certificate, etc. Including which ciphers were selected and more TLS details.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="e8f41e04bab94a5f953723915745646c">
<span data-offset-key="e8f41e04bab94a5f953723915745646c:0">In addition to the added information given from curl internals, the -v verbose mode will also make curl show all headers it sends and receives. For protocols without headers (like FTP, SMTP, POP3 and so on), we can consider commands and responses as headers and they will thus also be shown with -v.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="20b70d406e434d99a5956e527e8700b7">
<span data-offset-key="20b70d406e434d99a5956e527e8700b7:0">If we then continue the output seen from the command above (but ignore the actual HTML response), curl will show:</span>
</span>
</span>        > GET / HTTP/1.1    > Host: example.com    > User-Agent: curl/7.45.0    > Accept: */*    >
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="2921405fe5b64e6591ad8af4106ea024">
<span data-offset-key="2921405fe5b64e6591ad8af4106ea024:0">This is the full HTTP request to the site. This request is how it looks in a default curl 7.45.0 installation and it may, of course, differ slightly between different releases and in particular it will change if you add command line options.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="9e547c29ec2f435a954ebea71db9f56c">
<span data-offset-key="9e547c29ec2f435a954ebea71db9f56c:0">The last line of the HTTP request headers looks empty, and it is. It signals the separation between the headers and the body, and in this request there is no "body" to send.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="84517311d276494db9dc6cbb9b153825">
<span data-offset-key="84517311d276494db9dc6cbb9b153825:0">Moving on and assuming everything goes according to plan, the sent request will get a corresponding response from the server and that HTTP response will start with a set of headers before the response body:</span>
</span>
</span>    < HTTP/1.1 200 OK< Accept-Ranges: bytes< Cache-Control: max-age=604800< Content-Type: text/html< Date: Sat, 19 Dec 2015 22:01:03 GMT< Etag: "359670651"< Expires: Sat, 26 Dec 2015 22:01:03 GMT< Last-Modified: Fri, 09 Aug 2013 23:54:35 GMT< Server: ECS (ewr/15BD)< Vary: Accept-Encoding< X-Cache: HIT< x-ec-custom-error: 1< Content-Length: 1270<<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="19759e1392244c6b807b76469e361a7f">
<span data-offset-key="19759e1392244c6b807b76469e361a7f:0">This may look mostly like mumbo jumbo to you, but this is normal set of HTTP headers—metadata—about the response. The first line's "200" might be the most important piece of information in there and means "everything is fine".</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="090a1cc096f34745b0c9d212995f7639">
<span data-offset-key="090a1cc096f34745b0c9d212995f7639:0">The last line of the received headers is, as you can see, empty, and that is the marker used for the HTTP protocol to signal the end of the headers.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="8b1e791353614b27bfcda995b743ca46">
<span data-offset-key="8b1e791353614b27bfcda995b743ca46:0">After the headers comes the actual response body, the data payload. The regular -v verbose mode does not show that data but only displays</span>
</span>
</span>    { [1270 bytes data]<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="39874ecf128943fea10c2b091abc02d2">
<span data-offset-key="39874ecf128943fea10c2b091abc02d2:0">That 1270 bytes should then be in the 'saved' file. You can also see that there was a header named Content-Length: in the response that contained the exact file length (it will not always be present in responses).</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="e88112effa354ecbabcf419d43e5cf64">
<span data-offset-key="e88112effa354ecbabcf419d43e5cf64:0">HTTP/2 and HTTP/3</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="385ccb859c12413897f69ffd42e0fa2f">
<span data-offset-key="385ccb859c12413897f69ffd42e0fa2f:0">When doing file transfers using version two or three of the HTTP protocol, curl sends and receives </span>
<span data-offset-key="385ccb859c12413897f69ffd42e0fa2f:1">**compressed**</span>
<span data-offset-key="385ccb859c12413897f69ffd42e0fa2f:2"> headers. So to display outgoing and incoming HTTP/2 and HTTP/3 headers in a readable and understandable way, curl will actually show the uncompressed versions in a style similar to how they appear with HTTP/1.1.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="51079c8a546840a7b667d20668e18514">
<span data-offset-key="51079c8a546840a7b667d20668e18514:0">Silence</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="d0cc0780025b450f87451b253c84f2be">
<span data-offset-key="d0cc0780025b450f87451b253c84f2be:0">The opposite of verbose is, of course, to make curl more silent. With the </span>
<span data-offset-key="d0cc0780025b450f87451b253c84f2be:1">`-s`</span>
<span data-offset-key="d0cc0780025b450f87451b253c84f2be:2"> (or </span>
<span data-offset-key="d0cc0780025b450f87451b253c84f2be:3">`--silent`</span>
<span data-offset-key="d0cc0780025b450f87451b253c84f2be:4">) option you make curl switch off the progress meter and not output any error messages for when errors occur. It gets mute. It will still output the downloaded data you ask it to.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="6e0dbfef0516469288428b9e635890f0">
<span data-offset-key="6e0dbfef0516469288428b9e635890f0:0">With silence activated, you can ask for it to still output the error message on failures by adding </span>
<span data-offset-key="6e0dbfef0516469288428b9e635890f0:1">`-S`</span>
<span data-offset-key="6e0dbfef0516469288428b9e635890f0:2"> or </span>
<span data-offset-key="6e0dbfef0516469288428b9e635890f0:3">`--show-error`</span>
<span data-offset-key="6e0dbfef0516469288428b9e635890f0:4">.</span>
</span>
</span>
<a href="../usingcurl.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">
</a>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Using curl</span>
<a href="verbose/trace.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">
</a>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Trace options</span>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 1 year ago</span>
<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>
<a href="verbose.html#http-2-and-http-3" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">HTTP/2 and HTTP/3</span>
</span>
<a href="verbose.html#silence" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Silence</span>
</span>
