# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Write out</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="d62488f66c6e4fddb59da3d1519aa87e">

<span data-offset-key="d62488f66c6e4fddb59da3d1519aa87e:0">This is one of the often forgotten little gems in the curl arsenal of command line options. </span>

<span data-offset-key="d62488f66c6e4fddb59da3d1519aa87e:1">`--write-out`</span>

<span data-offset-key="d62488f66c6e4fddb59da3d1519aa87e:2"> or just </span>

<span data-offset-key="d62488f66c6e4fddb59da3d1519aa87e:3">`-w`</span>

<span data-offset-key="d62488f66c6e4fddb59da3d1519aa87e:4"> for short, writes out information after a transfer has completed and it has a large range of variables that you can include in the output, variables that have been set with values and information from the transfer.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ad7a400555464acca77639cd5e3aac4a">

<span data-offset-key="ad7a400555464acca77639cd5e3aac4a:0">You tell curl to write a string just by passing that string to this option:</span>

</span>

</span> curl -w "formatted string" http://example.com/<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="5a6d1183378b49eeb90d05e7cdf706b3">

<span data-offset-key="5a6d1183378b49eeb90d05e7cdf706b3:0">…and you can also have curl read that string from a given file instead if you prefix the string with '@':</span>

</span>

</span> curl -w @filename http://example.com/<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="d57d19cb57ce44c1b24a7722cc97120d">

<span data-offset-key="d57d19cb57ce44c1b24a7722cc97120d:0">…or even have curl read the string from stdin if you use '-' as filename:</span>

</span>

</span> curl -w @- http://example.com/<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="46c42b56c0894ab196ccac99b04e6998">

<span data-offset-key="46c42b56c0894ab196ccac99b04e6998:0">The variables that are available are accessed by writing </span>

<span data-offset-key="46c42b56c0894ab196ccac99b04e6998:1">`%{variable_name}`</span>

<span data-offset-key="46c42b56c0894ab196ccac99b04e6998:2"> in the string and that variable will then be substituted by the correct value. To output a normal '%' you just write it as '%%'. You can also output a newline by using '\\n', a carriage return with '\\r' and a tab space with '\\t'.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="d53e6bedb94141488a8d632c86d25fb7">

<span data-offset-key="d53e6bedb94141488a8d632c86d25fb7:0">(The %-symbol is special on the Windows command line, where all occurrences of % must be doubled when using this option.)</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="af825fd2a0d04a84b6408366db287b71">

<span data-offset-key="af825fd2a0d04a84b6408366db287b71:0">As an example, we can output the Content-Type and the response code from an HTTP transfer, separated with newlines and some extra text like this:</span>

</span>

</span> curl -w "Type: %{content_type}\nCode: %{response_code}\n" http://example.com<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="71381ee904174d47ad898044b1b16cf7">

<span data-offset-key="71381ee904174d47ad898044b1b16cf7:0">This feature writes the output to stdout so you probably want to make sure that you do not also send the downloaded content to stdout as then you might have a hard time to separate out the data.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="d6f9f53c24bf4a1986ed822f65bc53e8">

<span data-offset-key="d6f9f53c24bf4a1986ed822f65bc53e8:0">Available --write-out variables</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="d16d1b92122e403ca568a3d853b91028">

<span data-offset-key="d16d1b92122e403ca568a3d853b91028:0">Some of these variables are not available in really old curl versions.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="dee84225f4544c278d1db53a6160f3fa">

<span data-offset-key="dee84225f4544c278d1db53a6160f3fa:0">`%{content_type}`</span>

<span data-offset-key="dee84225f4544c278d1db53a6160f3fa:1"> the Content-Type of the requested document, if there was any.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8ba21bb0b0254ab59925419b1915845e">

<span data-offset-key="8ba21bb0b0254ab59925419b1915845e:0">`%{errormsg}`</span>

<span data-offset-key="8ba21bb0b0254ab59925419b1915845e:1"> the error message from the transfer. Empty if no error occured. (Introduced in 7.75.0)</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="66545b76442440c9b013f09779735fcc">

<span data-offset-key="66545b76442440c9b013f09779735fcc:0">`%{exitcode}`</span>

<span data-offset-key="66545b76442440c9b013f09779735fcc:1"> the numerical exit code from the transfer. 0 if no error occured. (Introduced in 7.75.0)</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f8cdc23acc8a4663a31fbd60bb24fb1b">

<span data-offset-key="f8cdc23acc8a4663a31fbd60bb24fb1b:0">`%{filename_effective}`</span>

<span data-offset-key="f8cdc23acc8a4663a31fbd60bb24fb1b:1"> the ultimate filename that curl writes out to. This is only meaningful if curl is told to write to a file with the </span>

<span data-offset-key="f8cdc23acc8a4663a31fbd60bb24fb1b:2">`--remote-name`</span>

<span data-offset-key="f8cdc23acc8a4663a31fbd60bb24fb1b:3"> or </span>

<span data-offset-key="f8cdc23acc8a4663a31fbd60bb24fb1b:4">`--output`</span>

<span data-offset-key="f8cdc23acc8a4663a31fbd60bb24fb1b:5"> option. It's most useful in combination with the </span>

<span data-offset-key="f8cdc23acc8a4663a31fbd60bb24fb1b:6">`--remote-header-name`</span>

<span data-offset-key="f8cdc23acc8a4663a31fbd60bb24fb1b:7"> option.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="dbddde0451ca4b32bd5255ef34220a3a">

<span data-offset-key="dbddde0451ca4b32bd5255ef34220a3a:0">`%{ftp_entry_path}`</span>

<span data-offset-key="dbddde0451ca4b32bd5255ef34220a3a:1"> the initial path curl ended up in when logging on to the remote FTP server.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="1712af33813b4d5d8307eef2c0559e8f">

<span data-offset-key="1712af33813b4d5d8307eef2c0559e8f:0">`%{http_code}`</span>

<span data-offset-key="1712af33813b4d5d8307eef2c0559e8f:1"> the old variable name for what is now known as </span>

<span data-offset-key="1712af33813b4d5d8307eef2c0559e8f:2">`response_code`</span>

<span data-offset-key="1712af33813b4d5d8307eef2c0559e8f:3">.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2690f1e2f18840359aa77550f863996e">

<span data-offset-key="2690f1e2f18840359aa77550f863996e:0">`%{http_connect}`</span>

<span data-offset-key="2690f1e2f18840359aa77550f863996e:1"> the numerical code that was found in the last response (from a proxy) to a curl CONNECT request.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="87fe8ad1339d46799e286dbbc84814a9">

<span data-offset-key="87fe8ad1339d46799e286dbbc84814a9:0">`%{http_version}`</span>

<span data-offset-key="87fe8ad1339d46799e286dbbc84814a9:1"> The http version that was used.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="90973dcd7f78445bbe200d2ac688b8ca">

<span data-offset-key="90973dcd7f78445bbe200d2ac688b8ca:0">`%{json}`</span>

<span data-offset-key="90973dcd7f78445bbe200d2ac688b8ca:1"> all write-out variables as a single JSON object.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c240c090be594f92800fcbf28f4145eb">

<span data-offset-key="c240c090be594f92800fcbf28f4145eb:0">`%{local_ip}`</span>

<span data-offset-key="c240c090be594f92800fcbf28f4145eb:1"> the IP address of the local end of the most recently done connection—can be either IPv4 or IPv6</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0b89ba25ca7e4a13b56ffbb1c7848680">

<span data-offset-key="0b89ba25ca7e4a13b56ffbb1c7848680:0">`%{local_port}`</span>

<span data-offset-key="0b89ba25ca7e4a13b56ffbb1c7848680:1"> the local port number of the most recently made connection</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e89da06dde7b451680692b02506f04c9">

<span data-offset-key="e89da06dde7b451680692b02506f04c9:0">`%{method}`</span>

<span data-offset-key="e89da06dde7b451680692b02506f04c9:1"> HTTP method the most recent request used</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="3617b8a4d00e4cb19456f05944e427ec">

<span data-offset-key="3617b8a4d00e4cb19456f05944e427ec:0">`%{num_connects}`</span>

<span data-offset-key="3617b8a4d00e4cb19456f05944e427ec:1"> the number of new connects made in the recent transfer.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="5da66b11534c403e86b08f972a4747c7">

<span data-offset-key="5da66b11534c403e86b08f972a4747c7:0">`%{num_headers}`</span>

<span data-offset-key="5da66b11534c403e86b08f972a4747c7:1"> number of response headers in the last responsea</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4e03475c8afe41e09f0434f13c5d1084">

<span data-offset-key="4e03475c8afe41e09f0434f13c5d1084:0">`%{num_redirects}`</span>

<span data-offset-key="4e03475c8afe41e09f0434f13c5d1084:1"> number of redirects that were followed in the request.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="166bcc113ef5469b8994b9471eb1bbc4">

<span data-offset-key="166bcc113ef5469b8994b9471eb1bbc4:0">`%{onerror}`</span>

<span data-offset-key="166bcc113ef5469b8994b9471eb1bbc4:1"> if the transfer ended with an error, show the rest of the string, otherwise stop here. (Introduced in 7.75.0)</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="390662d27e9c45e484790c21845f2766">

<span data-offset-key="390662d27e9c45e484790c21845f2766:0">`%{proxy_ssl_verify_result}`</span>

<span data-offset-key="390662d27e9c45e484790c21845f2766:1"> the result of the SSL peer certificate verification that was requested when communicating with a proxy. 0 means the verification was successful.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="913f3a36eff74751b58dcad31e411b7b">

<span data-offset-key="913f3a36eff74751b58dcad31e411b7b:0">`%{redirect_url}`</span>

<span data-offset-key="913f3a36eff74751b58dcad31e411b7b:1"> the actual URL a redirect </span>

<span data-offset-key="913f3a36eff74751b58dcad31e411b7b:2">_would_</span>

<span data-offset-key="913f3a36eff74751b58dcad31e411b7b:3"> take you to when an HTTP request was made without </span>

<span data-offset-key="913f3a36eff74751b58dcad31e411b7b:4">`-L`</span>

<span data-offset-key="913f3a36eff74751b58dcad31e411b7b:5"> to follow redirects.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a484a25fdb4d4571a7099f7de0dee0e8">

<span data-offset-key="a484a25fdb4d4571a7099f7de0dee0e8:0">`%{remote_ip}`</span>

<span data-offset-key="a484a25fdb4d4571a7099f7de0dee0e8:1"> the remote IP address of the most recently made connection—can be either IPv4 or IPv6.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7c4837f1cfb947bcbd51695b386194c6">

<span data-offset-key="7c4837f1cfb947bcbd51695b386194c6:0">`%{remote_port}`</span>

<span data-offset-key="7c4837f1cfb947bcbd51695b386194c6:1"> the remote port number of the most recently made connection.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="3ab7553e4a454bdeab5225ac0992e0c1">

<span data-offset-key="3ab7553e4a454bdeab5225ac0992e0c1:0">`%{response_code}`</span>

<span data-offset-key="3ab7553e4a454bdeab5225ac0992e0c1:1"> the numerical response code that was found in the last transfer.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ee2b60650ec84169a21241bd78fbfd07">

<span data-offset-key="ee2b60650ec84169a21241bd78fbfd07:0">`%{scheme}`</span>

<span data-offset-key="ee2b60650ec84169a21241bd78fbfd07:1"> scheme used in the previous URL</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="49efa41d19084bbb97c17a5bae0e0b65">

<span data-offset-key="49efa41d19084bbb97c17a5bae0e0b65:0">`%{size_download}`</span>

<span data-offset-key="49efa41d19084bbb97c17a5bae0e0b65:1"> the total number of bytes that were downloaded.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a881e9b2eecf485286e3a77c9e290128">

<span data-offset-key="a881e9b2eecf485286e3a77c9e290128:0">`%{size_header}`</span>

<span data-offset-key="a881e9b2eecf485286e3a77c9e290128:1"> the total number of bytes of the downloaded headers.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a36fb10b37074487b94aca14d5a5bd2d">

<span data-offset-key="a36fb10b37074487b94aca14d5a5bd2d:0">`%{size_request}`</span>

<span data-offset-key="a36fb10b37074487b94aca14d5a5bd2d:1"> the total number of bytes that were sent in the HTTP request.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6538f4b041324a2c8748a90fb4355e85">

<span data-offset-key="6538f4b041324a2c8748a90fb4355e85:0">`%{size_upload}`</span>

<span data-offset-key="6538f4b041324a2c8748a90fb4355e85:1"> the total number of bytes that were uploaded.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="da59e695c6ac4091af498aaeb6be2414">

<span data-offset-key="da59e695c6ac4091af498aaeb6be2414:0">`%{speed_download}`</span>

<span data-offset-key="da59e695c6ac4091af498aaeb6be2414:1"> the average download speed that curl measured for the complete download in bytes per second.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="99d3a4dfa5614eebb22a3cc4febb92c4">

<span data-offset-key="99d3a4dfa5614eebb22a3cc4febb92c4:0">`%{speed_upload}`</span>

<span data-offset-key="99d3a4dfa5614eebb22a3cc4febb92c4:1"> the average upload speed that curl measured for the complete upload in bytes per second.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6cc5cbaff8a3431aafb8cec15509c667">

<span data-offset-key="6cc5cbaff8a3431aafb8cec15509c667:0">`%{ssl_verify_result}`</span>

<span data-offset-key="6cc5cbaff8a3431aafb8cec15509c667:1"> the result of the SSL peer certificate verification that was requested. 0 means the verification was successful.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="7dca5032b13b4c7a9cf1cb57022f04df">

<span data-offset-key="7dca5032b13b4c7a9cf1cb57022f04df:0">`%{stderr}`</span>

<span data-offset-key="7dca5032b13b4c7a9cf1cb57022f04df:1"> - makes the rest of the output get written to stderr.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="af149b582ce943b7bf6e1ce66c0f0124">

<span data-offset-key="af149b582ce943b7bf6e1ce66c0f0124:0">`%{stdout}`</span>

<span data-offset-key="af149b582ce943b7bf6e1ce66c0f0124:1"> - makes the rest of the output get written to stdout.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c69189a991674aaa928c209cc23e31ea">

<span data-offset-key="c69189a991674aaa928c209cc23e31ea:0">`%{time_appconnect}`</span>

<span data-offset-key="c69189a991674aaa928c209cc23e31ea:1"> the time, in seconds, it took from the start until the SSL/SSH/etc connect/handshake to the remote host was completed.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c75023fa679b42eab34dcd146f582ea5">

<span data-offset-key="c75023fa679b42eab34dcd146f582ea5:0">`%{time_connect}`</span>

<span data-offset-key="c75023fa679b42eab34dcd146f582ea5:1"> the time, in seconds, it took from the start until the TCP connect to the remote host (or proxy) was completed.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="07c945c8fa354f55bfad82ab57cf5df6">

<span data-offset-key="07c945c8fa354f55bfad82ab57cf5df6:0">`%{time_namelookup}`</span>

<span data-offset-key="07c945c8fa354f55bfad82ab57cf5df6:1"> the time, in seconds, it took from the start until the name resolving was completed.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6d8360a519674cfe9e38b7cb3a213728">

<span data-offset-key="6d8360a519674cfe9e38b7cb3a213728:0">`%{time_pretransfer}`</span>

<span data-offset-key="6d8360a519674cfe9e38b7cb3a213728:1"> the time, in seconds, it took from the start until the file transfer was just about to begin. This includes all pre-transfer commands and negotiations that are specific to the particular protocol(s) involved.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="18e9ccc06bba4ce69f32e9fc5f44c5d3">

<span data-offset-key="18e9ccc06bba4ce69f32e9fc5f44c5d3:0">`%{time_redirect}`</span>

<span data-offset-key="18e9ccc06bba4ce69f32e9fc5f44c5d3:1"> the time, in seconds, it took for all redirection steps including name lookup, connect, pre-transfer and transfer before the final transaction was started. time_redirect the complete execution time for multiple redirections.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f6d93fda3f7f4b48b5f90a48a7ab3ceb">

<span data-offset-key="f6d93fda3f7f4b48b5f90a48a7ab3ceb:0">`%{time_starttransfer}`</span>

<span data-offset-key="f6d93fda3f7f4b48b5f90a48a7ab3ceb:1"> the time, in seconds, it took from the start until the first byte was just about to be transferred. This includes time_pretransfer and also the time the server needed to calculate the result.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="1aa5e9ad9c934e39a5713d763b8e2382">

<span data-offset-key="1aa5e9ad9c934e39a5713d763b8e2382:0">`%{time_total}`</span>

<span data-offset-key="1aa5e9ad9c934e39a5713d763b8e2382:1"> the total time, in seconds, that the full operation lasted. The time will be displayed with millisecond resolution.</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="66441cb692444dac9509455989882852">

<span data-offset-key="66441cb692444dac9509455989882852:0">`%{url}`</span>

<span data-offset-key="66441cb692444dac9509455989882852:1"> the URL used in the transfer. (Introduced in 7.75.0)</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e55d576883094493aa4e8e12920eefa1">

<span data-offset-key="e55d576883094493aa4e8e12920eefa1:0">`%{url_effective}`</span>

<span data-offset-key="e55d576883094493aa4e8e12920eefa1:1"> the URL that was fetched last. This is particularly meaningful if you have told curl to follow Location: headers (with </span>

<span data-offset-key="e55d576883094493aa4e8e12920eefa1:2">`-L`</span>

<span data-offset-key="e55d576883094493aa4e8e12920eefa1:3">).</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="89459dc7b3ad4818a4f05740b6e25c97">

<span data-offset-key="89459dc7b3ad4818a4f05740b6e25c97:0">`%{urlnum}`</span>

<span data-offset-key="89459dc7b3ad4818a4f05740b6e25c97:1"> the 0-based numerical index of the URL used in the transfer. (Introduced in 7.75.0)</span>

</span>

</span>

<a href="trace.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Trace options</span>
