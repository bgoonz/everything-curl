<a href="timeouts.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

</a>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Timeouts</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="303180c511754cb99c0dc8476165354e">

<span data-offset-key="303180c511754cb99c0dc8476165354e:0">Network operations are by their nature rather unreliable or perhaps fragile operations as they depend on a set of services and networks to be up and working for things to work. The availability of these services can come and go and the performance of them may also vary greatly from time to time.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4a921b3d7d4f46a58b6479664b73732b">

<span data-offset-key="4a921b3d7d4f46a58b6479664b73732b:0">The design of TCP even allows the network to get completely disconnected for an extended period of time without it necessarily getting noticed by the participants in the transfer.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6162bab433b845e9a954d96e39d9487c">

<span data-offset-key="6162bab433b845e9a954d96e39d9487c:0">The result of this is that sometimes Internet transfers take a long time. Further, most operations in curl have no time-out by default!</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="c5c3ad885c8141a58004e3267129f865">

<span data-offset-key="c5c3ad885c8141a58004e3267129f865:0">Maximum time allowed to spend</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="30e70c7e0ea34290bfd50d419b1d9175">

<span data-offset-key="30e70c7e0ea34290bfd50d419b1d9175:0">Tell curl with </span>

<span data-offset-key="30e70c7e0ea34290bfd50d419b1d9175:1">`-m / --max-time`</span>

<span data-offset-key="30e70c7e0ea34290bfd50d419b1d9175:2"> the maximum time, in seconds, that you allow the command line to spend before curl exits with a timeout error code (28). When the set time has elapsed, curl will exit no matter what is going on at that moment—including if it is transferring data. It really is the maximum time allowed.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="055496cbc211458fae9aaf97c3f430b0">

<span data-offset-key="055496cbc211458fae9aaf97c3f430b0:0">The given maximum time can be specified with a decimal precision; </span>

<span data-offset-key="055496cbc211458fae9aaf97c3f430b0:1">`0.5`</span>

<span data-offset-key="055496cbc211458fae9aaf97c3f430b0:2"> means 500 milliseconds and </span>

<span data-offset-key="055496cbc211458fae9aaf97c3f430b0:3">`2.37`</span>

<span data-offset-key="055496cbc211458fae9aaf97c3f430b0:4"> equals 2370 milliseconds.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b02aa0945e7f4fa8a07e03bb81ac6e10">

<span data-offset-key="b02aa0945e7f4fa8a07e03bb81ac6e10:0">Example:</span>

</span>

</span> curl --max-time 5.5 https://example.com/<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="bdb0545a8a5645cbaf5f3fd3fc7c9eec">

<span data-offset-key="bdb0545a8a5645cbaf5f3fd3fc7c9eec:0">(Your locale may use another symbol than a dot for expressing numerical fractions.)</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="2204a4c2395543d1b38d62db408e9816">

<span data-offset-key="2204a4c2395543d1b38d62db408e9816:0">Never spend more than this to connect</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="09e95f6859ca429fa20132722c2bb623">

<span data-offset-key="09e95f6859ca429fa20132722c2bb623:0">`--connect-timeout`</span>

<span data-offset-key="09e95f6859ca429fa20132722c2bb623:1"> limits the time curl will spend trying to connect to the host. All the necessary steps done before the connection is considered complete have to be completed within the given time frame. Failing to connect within the given time will cause curl to exit with a timeout exit code (28).</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="38452b90f0ad4d0287dbec86033137be">

<span data-offset-key="38452b90f0ad4d0287dbec86033137be:0">The given maximum connect time can be specified with a decimal precision; </span>

<span data-offset-key="38452b90f0ad4d0287dbec86033137be:1">`0.5`</span>

<span data-offset-key="38452b90f0ad4d0287dbec86033137be:2"> means 500 milliseconds and </span>

<span data-offset-key="38452b90f0ad4d0287dbec86033137be:3">`2.37`</span>

<span data-offset-key="38452b90f0ad4d0287dbec86033137be:4"> equals 2370 milliseconds:</span>

</span>

</span> curl --connect-timeout 2.37 https://example.com/<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="1557047690134a87988150d8afeecbc6">

<span data-offset-key="1557047690134a87988150d8afeecbc6:0">Transfer speeds slower than this means exit</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="1d1df564788b46a2b0e729145a76daed">

<span data-offset-key="1d1df564788b46a2b0e729145a76daed:0">Having a fixed maximum time for a curl operation can be cumbersome, especially if you, for example, do scripted transfers and the file sizes and transfer times vary a lot. A fixed timeout value then needs to be set unnecessarily high to cover for worst cases.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8d4c31ef0b8d4490a87af7c47bfe87f0">

<span data-offset-key="8d4c31ef0b8d4490a87af7c47bfe87f0:0">As an alternative to a fixed time-out, you can tell curl to abandon the transfer if it gets below a certain speed and stays below that threshold for a specific period of time.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9f05a7e014c440e1b3ee5ae6fce3af1f">

<span data-offset-key="9f05a7e014c440e1b3ee5ae6fce3af1f:0">For example, if a transfer speed goes below 1000 bytes per second during 15 seconds, stop it:</span>

</span>

</span> curl --speed-time 15 --speed-limit 1000 https://example.com/<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="26f7a19d7e894073ac43f5ba8c43e178">

<span data-offset-key="26f7a19d7e894073ac43f5ba8c43e178:0">Keep connections alive</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e13fcd4a276c4535a498e7daa56881fc">

<span data-offset-key="e13fcd4a276c4535a498e7daa56881fc:0">curl enables TCP keep-alive by default. TCP keep-alive is a feature that makes the TCP stack send a probe to the other side when there's no traffic, to make sure that it is still there and "alive". By using keep-alive, curl is much more likely to discover that the TCP connection is dead.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4b6e30e4c26f460889211aaa70e2ec24">

<span data-offset-key="4b6e30e4c26f460889211aaa70e2ec24:0">Use </span>

<span data-offset-key="4b6e30e4c26f460889211aaa70e2ec24:1">`--keepalive-time`</span>

<span data-offset-key="4b6e30e4c26f460889211aaa70e2ec24:2"> to specify how often in full seconds you would like the probe to get sent to the peer. The default value is 60 seconds.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6c5c783846a64d1d9b165b0c76577cd6">

<span data-offset-key="6c5c783846a64d1d9b165b0c76577cd6:0">Sometimes this probing disturbs what you are doing and then you can easily disable it with </span>

<span data-offset-key="6c5c783846a64d1d9b165b0c76577cd6:1">`--no-keepalive`</span>

<span data-offset-key="6c5c783846a64d1d9b165b0c76577cd6:2">.</span>

</span>

</span>

<a href="connections.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Connections</span>

<a href="netrc.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">.netrc</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="timeouts.html#maximum-time-allowed-to-spend" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Maximum time allowed to spend</span>

</span>

<a href="timeouts.html#never-spend-more-than-this-to-connect" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Never spend more than this to connect</span>

</span>

<a href="timeouts.html#transfer-speeds-slower-than-this-means-exit" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Transfer speeds slower than this means exit</span>

</span>

<a href="timeouts.html#keep-connections-alive" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Keep connections alive</span>

</span>
