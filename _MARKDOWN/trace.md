







<a href="trace.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Trace options</span></a>

<a href="writeout.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Write out</span></a>

<a href="../version.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Version</span></a>

<a href="../persist.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca"><span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Persistent connections</span></a>















# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Trace options</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2"></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="c47a63eb63b94ec497e15ed367a3313b"><span data-offset-key="c47a63eb63b94ec497e15ed367a3313b:0">There are times when </span><span data-offset-key="c47a63eb63b94ec497e15ed367a3313b:1">`-v`</span><span data-offset-key="c47a63eb63b94ec497e15ed367a3313b:2"> is not enough. In particular, when you want to store the complete stream including the actual transferred data.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="79f7332dd6bf466aacd76677ded40423"><span data-offset-key="79f7332dd6bf466aacd76677ded40423:0">For situations when curl does encrypted file transfers with protocols such as HTTPS, FTPS or SFTP, other network monitoring tools (like Wireshark or tcpdump) will not be able to do this job as easily for you.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="388656d103e64ea080c159503ff14673"><span data-offset-key="388656d103e64ea080c159503ff14673:0">For this, curl offers two other options that you use instead of </span><span data-offset-key="388656d103e64ea080c159503ff14673:1">`-v`</span><span data-offset-key="388656d103e64ea080c159503ff14673:2">.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="971b082de53d4f43b1fbd479951ad5dd"><span data-offset-key="971b082de53d4f43b1fbd479951ad5dd:0">`--trace [filename]`</span><span data-offset-key="971b082de53d4f43b1fbd479951ad5dd:1"> will save a full trace in the given file name. You can also use '-' (a single minus) instead of a file name to get it passed to stdout. You would use it like this:</span></span></span>

    $ curl --trace dump http://example.com

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="005bd2da5cdc4f1485025d85c8f20bf3"><span data-offset-key="005bd2da5cdc4f1485025d85c8f20bf3:0">When completed, there's a 'dump' file that can turn out pretty sizable. In this case, the 15 first lines of the dump file looks like:</span></span></span>

    == Info: Rebuilt URL to: http://example.com/== Info:   Trying 93.184.216.34...== Info: Connected to example.com (93.184.216.34) port 80 (#0)=> Send header, 75 bytes (0x4b)0000: 47 45 54 20 2f 20 48 54 54 50 2f 31 2e 31 0d 0a GET / HTTP/1.1..0010: 48 6f 73 74 3a 20 65 78 61 6d 70 6c 65 2e 63 6f Host: example.co0020: 6d 0d 0a 55 73 65 72 2d 41 67 65 6e 74 3a 20 63 m..User-Agent: c0030: 75 72 6c 2f 37 2e 34 35 2e 30 0d 0a 41 63 63 65 url/7.45.0..Acce0040: 70 74 3a 20 2a 2f 2a 0d 0a 0d 0a                pt: */*....<= Recv header, 17 bytes (0x11)0000: 48 54 54 50 2f 31 2e 31 20 32 30 30 20 4f 4b 0d HTTP/1.1 200 OK.0010: 0a                                              .<= Recv header, 22 bytes (0x16)0000: 41 63 63 65 70 74 2d 52 61 6e 67 65 73 3a 20 62 Accept-Ranges: b0010: 79 74 65 73 0d 0a                               ytes..

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="40a899c38f7b4a98a7387c1526a19730"><span data-offset-key="40a899c38f7b4a98a7387c1526a19730:0">Every single sent and received byte get displayed individually in hexadecimal numbers.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="aa4dc13ee63040aab0c0303f6f7e5650"><span data-offset-key="aa4dc13ee63040aab0c0303f6f7e5650:0">If you think the hexadecimals are not helping, you can try </span><span data-offset-key="aa4dc13ee63040aab0c0303f6f7e5650:1">`--trace-ascii [filename]`</span><span data-offset-key="aa4dc13ee63040aab0c0303f6f7e5650:2"> instead, also this accepting '-' for stdout and that makes the 15 first lines of tracing look like:</span></span></span>

    == Info: Rebuilt URL to: http://example.com/== Info:   Trying 93.184.216.34...== Info: Connected to example.com (93.184.216.34) port 80 (#0)=> Send header, 75 bytes (0x4b)0000: GET / HTTP/1.10010: Host: example.com0023: User-Agent: curl/7.45.0003c: Accept: */*0049:<= Recv header, 17 bytes (0x11)0000: HTTP/1.1 200 OK<= Recv header, 22 bytes (0x16)0000: Accept-Ranges: bytes<= Recv header, 31 bytes (0x1f)0000: Cache-Control: max-age=604800

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1"><span data-key="3d39520935f645aa8dadf8545c8edc2e"><span data-offset-key="3d39520935f645aa8dadf8545c8edc2e:0">--trace-time</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="45a9708d34fa4752b596d88b6c328371"><span data-offset-key="45a9708d34fa4752b596d88b6c328371:0">This options prefixes all verbose/trace outputs with a high resolution timer for when the line is printed. It works with the regular </span><span data-offset-key="45a9708d34fa4752b596d88b6c328371:1">`-v / --verbose`</span><span data-offset-key="45a9708d34fa4752b596d88b6c328371:2"> option as well as with </span><span data-offset-key="45a9708d34fa4752b596d88b6c328371:3">`--trace`</span><span data-offset-key="45a9708d34fa4752b596d88b6c328371:4"> and </span><span data-offset-key="45a9708d34fa4752b596d88b6c328371:5">`--trace-ascii`</span><span data-offset-key="45a9708d34fa4752b596d88b6c328371:6">.</span></span></span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="d1a95ff5f69a4df297db6d12ca769d30"><span data-offset-key="d1a95ff5f69a4df297db6d12ca769d30:0">An example could look like this:</span></span></span>

    $ curl -v --trace-time http://example.com23:38:56.837164 * Rebuilt URL to: http://example.com/23:38:56.841456 *   Trying 93.184.216.34...23:38:56.935155 * Connected to example.com (93.184.216.34) port 80 (#0)23:38:56.935296 > GET / HTTP/1.123:38:56.935296 > Host: example.com23:38:56.935296 > User-Agent: curl/7.45.023:38:56.935296 > Accept: */*23:38:56.935296 >23:38:57.029570 < HTTP/1.1 200 OK23:38:57.029699 < Accept-Ranges: bytes23:38:57.029803 < Cache-Control: max-age=60480023:38:57.029903 < Content-Type: text/html---- snip ----

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1"><span data-key="4c19bbee96c14e618d2e5b80ae437f5b"><span data-offset-key="4c19bbee96c14e618d2e5b80ae437f5b:0">The lines are all the local time as hours:minutes:seconds and then number of microseconds in that second.</span></span></span>

<a href="../verbose.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674"></a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Verbose</span>

<a href="writeout.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42"></a>


<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Write out</span>



<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>


