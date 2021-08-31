<a href="options.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Command line options</span>
</a>
<a href="versions.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Options depend on version</span>
</a>
<a href="urls.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">URLs</span>
</a>
<a href="globbing.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">URL globbing</span>
</a>
<a href="listopts.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">List options</span>
</a>
<a href="configfile.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Config file</span>
</a>
<a href="passwords.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Passwords</span>
</a>
<a href="progressmeter.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Progress meter</span>
</a># <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Progress meter</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="e1e0b093d45942f794e50666aee31555">
<span data-offset-key="e1e0b093d45942f794e50666aee31555:0">curl has a built-in progress meter. When curl is invoked to transfer data (either uploading or downloading) it can show that meter in the terminal screen to show how the transfer is progressing, namely the current transfer speed, how long it has been going on and how long it thinks it might be left until completion.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="e1d2b4779eb246ac8c43e19465195857">
<span data-offset-key="e1d2b4779eb246ac8c43e19465195857:0">The progress meter is inhibited if curl deems that there is output going to the terminal, as the progress meter would interfere with that output and just mess up what gets displayed. A user can also forcibly switch off the progress meter with the </span>
<span data-offset-key="e1d2b4779eb246ac8c43e19465195857:1">`-s / --silent`</span>
<span data-offset-key="e1d2b4779eb246ac8c43e19465195857:2"> option, which tells curl to hush.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="fbe59381b0e64f6ab1a6df553f587d8c">
<span data-offset-key="fbe59381b0e64f6ab1a6df553f587d8c:0">If you invoke curl and do not get the progress meter, make sure your output is directed somewhere other than the terminal.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="c2a23e1dc87a439d95315f0fd76f762a">
<span data-offset-key="c2a23e1dc87a439d95315f0fd76f762a:0">curl also features an alternative and simpler progress meter that you enable with </span>
<span data-offset-key="c2a23e1dc87a439d95315f0fd76f762a:1">`-# / --progress-bar`</span>
<span data-offset-key="c2a23e1dc87a439d95315f0fd76f762a:2">. As the long name implies, it instead shows the transfer as progress bar.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="c3005949df5b47bfbb4823b427434205">
<span data-offset-key="c3005949df5b47bfbb4823b427434205:0">At times when curl is asked to transfer data, it cannot figure out the total size of the requested operation and that then subsequently makes the progress meter contain fewer details and it cannot, for example, make forecasts for transfer times, etc.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="2c34cef0de0c440fbd26b151bc846c7c">
<span data-offset-key="2c34cef0de0c440fbd26b151bc846c7c:0">Units</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="92e87e3869ed48c08c0cebbf5b351519">
<span data-offset-key="92e87e3869ed48c08c0cebbf5b351519:0">The progress meter displays bytes and bytes per second.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="8908065f2584417ea76ab67cfaee3a48">
<span data-offset-key="8908065f2584417ea76ab67cfaee3a48:0">It will also use suffixes for larger amounts of bytes, using the 1024 base system so 1024 is one kilobyte (1K), 2048 is 2K, etc. curl supports these:</span>
</span>
</span>
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td style="text-align: left;">
<p>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">
<span data-key="7c1dce79447747e8aeea097382b976ed">
<span data-offset-key="7c1dce79447747e8aeea097382b976ed:0">Suffix</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">
<span data-key="9955638b09ae44aeac253f6c97f84381">
<span data-offset-key="9955638b09ae44aeac253f6c97f84381:0">Amount</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">
<span data-key="960b9868e98549d49585ead866a316ee">
<span data-offset-key="960b9868e98549d49585ead866a316ee:0">Name</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="even">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="6027912143904b29966fa618a9e2df89">
<span data-offset-key="6027912143904b29966fa618a9e2df89:0">K</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="d0acdc0ccb9b49ffa88ee40d5682bb4a">
<span data-offset-key="d0acdc0ccb9b49ffa88ee40d5682bb4a:0">2^10</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="f0fc64e3d2ba45f5a949f69db3c7558e">
<span data-offset-key="f0fc64e3d2ba45f5a949f69db3c7558e:0">kilobyte</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="odd">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="783dc729b08148279c9e72732eb4ba81">
<span data-offset-key="783dc729b08148279c9e72732eb4ba81:0">M</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="ec04f2c9c951436db9cf55f4ab484679">
<span data-offset-key="ec04f2c9c951436db9cf55f4ab484679:0">2^20</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="b1c13cca4443416aa4c4298f8390dc82">
<span data-offset-key="b1c13cca4443416aa4c4298f8390dc82:0">megabyte</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="even">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="434568d0fd574cb0af590e19291add68">
<span data-offset-key="434568d0fd574cb0af590e19291add68:0">G</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="3fa9d130c48d4c5a8bd671a9e20651ff">
<span data-offset-key="3fa9d130c48d4c5a8bd671a9e20651ff:0">2^30</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="d7fc84f1492446b7a6945106c850bc28">
<span data-offset-key="d7fc84f1492446b7a6945106c850bc28:0">gigabyte</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="odd">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="56d40ee1438b4ad28cffd1e41ca046b5">
<span data-offset-key="56d40ee1438b4ad28cffd1e41ca046b5:0">T</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="3cc7e5b3697644a3bb15bc0e5812603b">
<span data-offset-key="3cc7e5b3697644a3bb15bc0e5812603b:0">2^40</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="549b291735de42ee9eaecb1b3238f7b8">
<span data-offset-key="549b291735de42ee9eaecb1b3238f7b8:0">terabyte</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="even">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="af2eac4e0d784653a31f2195ce8cf865">
<span data-offset-key="af2eac4e0d784653a31f2195ce8cf865:0">P</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="ff19430bfafa45679980056b374b473b">
<span data-offset-key="ff19430bfafa45679980056b374b473b:0">2^50</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="2b9982776c2b4b729da0230b3eb7ffa7">
<span data-offset-key="2b9982776c2b4b729da0230b3eb7ffa7:0">petabyte</span>
</span>
</span>
</p>
</td>
</tr>
</tbody>
</table>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="ef1398aa73214d0681b7a44d962bcb39">
<span data-offset-key="ef1398aa73214d0681b7a44d962bcb39:0">The times are displayed using H:MM:SS for hours, minutes and seconds.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="7ba85c1d3afe4a7784815c54968ad574">
<span data-offset-key="7ba85c1d3afe4a7784815c54968ad574:0">Progress meter legend</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="390d829689fc4399838049321b871664">
<span data-offset-key="390d829689fc4399838049321b871664:0">The progress meter exists to show a user that something actually is happening. The different fields in the output have the following meaning:</span>
</span>
</span>    % Total    % Received % Xferd  Average Speed          Time             Curr.                               Dload  Upload Total    Current  Left    Speed0  151M    0 38608    0     0   9406      0  4:41:43  0:00:04  4:41:39  9287<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="dd7fa39f953048d0ad148fff0add1835">
<span data-offset-key="dd7fa39f953048d0ad148fff0add1835:0">From left to right:</span>
</span>
</span>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td style="text-align: left;">
<p>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">
<span data-key="067977e7b5bb476aacdac1945944da30">
<span data-offset-key="067977e7b5bb476aacdac1945944da30:0">Title</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">
<span data-key="0668d01e59d849c68cb4403f44e6aba2">
<span data-offset-key="0668d01e59d849c68cb4403f44e6aba2:0">Meaning</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="even">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="48c3a18ca6ad4f35aa201e7cc83fc5f5">
<span data-offset-key="48c3a18ca6ad4f35aa201e7cc83fc5f5:0">%</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="05319fa9476244aa8d3461a28a8fd795">
<span data-offset-key="05319fa9476244aa8d3461a28a8fd795:0">Percentage completed of the whole transfer</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="odd">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="6afa2d61f86943da8738e9fb81bb3566">
<span data-offset-key="6afa2d61f86943da8738e9fb81bb3566:0">Total</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="34421ebc12704189bb7176d3287c906a">
<span data-offset-key="34421ebc12704189bb7176d3287c906a:0">Total size of the whole expected transfer (if known)</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="even">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="dbaff83e955a4554b05177b977bd3359">
<span data-offset-key="dbaff83e955a4554b05177b977bd3359:0">%</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="543cbe1d1dfb42eb9e4550daa1f8705f">
<span data-offset-key="543cbe1d1dfb42eb9e4550daa1f8705f:0">Percentage completed of the download</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="odd">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="087c2e292b834acb8f676cc8afb26457">
<span data-offset-key="087c2e292b834acb8f676cc8afb26457:0">Received</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="6a6f803e2d514dcea554f80b5b1b666d">
<span data-offset-key="6a6f803e2d514dcea554f80b5b1b666d:0">Currently downloaded number of bytes</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="even">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="0769ca6c17114296b54056a65d518c52">
<span data-offset-key="0769ca6c17114296b54056a65d518c52:0">%</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="c9d2c95eaa914efb93493488af3a3e5f">
<span data-offset-key="c9d2c95eaa914efb93493488af3a3e5f:0">Percentage completed of the upload</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="odd">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="3d8cfcd1bacd4b119b01f018105eab67">
<span data-offset-key="3d8cfcd1bacd4b119b01f018105eab67:0">Xferd</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="005740611564456ea9469ff69db2ea7e">
<span data-offset-key="005740611564456ea9469ff69db2ea7e:0">Currently uploaded number of bytes</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="even">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="f03bb8afc5e946b3810cdbbc6bc329cd">
<span data-offset-key="f03bb8afc5e946b3810cdbbc6bc329cd:0">Average Speed Dload</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="c44e8c13e7e9471582ed50b3d4cda5d2">
<span data-offset-key="c44e8c13e7e9471582ed50b3d4cda5d2:0">Average transfer speed of the entire download so far, in number of bytes per second</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="odd">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="ddb4751571904bb1ae1745e73e35125c">
<span data-offset-key="ddb4751571904bb1ae1745e73e35125c:0">Average Speed Upload</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="135ff02493b444f882a07d8c3a6da7f4">
<span data-offset-key="135ff02493b444f882a07d8c3a6da7f4:0">Average transfer speed of the entire upload so far, in number of bytes per second</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="even">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="9e549c80d68f4775b63de25023858262">
<span data-offset-key="9e549c80d68f4775b63de25023858262:0">Time Total</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="a2dc5a645bf643b7bda2a09a8549fe31">
<span data-offset-key="a2dc5a645bf643b7bda2a09a8549fe31:0">Expected time to complete the operation, in HH:MM:SS notation for hours, minutes and seconds</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="odd">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="1185627e6424491ca77f4b2da03af229">
<span data-offset-key="1185627e6424491ca77f4b2da03af229:0">Time Current</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="7c8495d0b37a460c828b7185b3851a48">
<span data-offset-key="7c8495d0b37a460c828b7185b3851a48:0">Time passed since the start of the transfer, in HH:MM:SS notation for hours, minutes and seconds</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="even">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="0c78fabff9a14ee2833bdeded740719f">
<span data-offset-key="0c78fabff9a14ee2833bdeded740719f:0">Time Left</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="88af0c9fa5ce451d8913f253b69850c2">
<span data-offset-key="88af0c9fa5ce451d8913f253b69850c2:0">Expected time left to completion, in HH:MM:SS notation for hours, minutes and seconds</span>
</span>
</span>
</p>
</td>
</tr>
<tr class="odd">
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="2e82937a1cce4007b9b039bdfd11ee99">
<span data-offset-key="2e82937a1cce4007b9b039bdfd11ee99:0">Curr.Speed</span>
</span>
</span>
</p>
</td>
<td style="text-align: left;">
<p>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="c6c7bf9129114c4ba0907455e40e03b7">
<span data-offset-key="c6c7bf9129114c4ba0907455e40e03b7:0">Average transfer speed over the last 5 seconds (the first 5 seconds of a transfer is based on less time, of course) in number of bytes per second</span>
</span>
</span>
</p>
</td>
</tr>
</tbody>
</table>
<a href="passwords.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">
</a>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Passwords</span>
<a href="../usingcurl.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">
</a>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Using curl</span>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 2 years ago</span>
<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>
<a href="progressmeter.html#units" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Units</span>
</span>
<a href="progressmeter.html#progress-meter-legend" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Progress meter legend</span>
</span>
