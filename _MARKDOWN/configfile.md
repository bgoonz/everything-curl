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

<a href="configfile.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Config file</span>

</a>

<a href="passwords.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Passwords</span>

</a>

<a href="progressmeter.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Progress meter</span>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Config file</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6183b486cacc4c5fbc3b04338ddc84c9">

<span data-offset-key="6183b486cacc4c5fbc3b04338ddc84c9:0">You can easily end up with curl command lines that use a large number of command-line options, making them rather hard to work with. Sometimes the length of the command line you want to enter even hits the maximum length your command-line system allows. The Microsoft Windows command prompt being an example of something that has a fairly small maximum line length.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8ae2f7fcd79349d096fd92dfab1059c5">

<span data-offset-key="8ae2f7fcd79349d096fd92dfab1059c5:0">To aid such situations, curl offers a feature we call "config file". It allows you to write command-line options in a text file instead and then tell curl to read options from that file in addition to the command line.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="1c3ae8ca4d294d12a21df05376efcf60">

<span data-offset-key="1c3ae8ca4d294d12a21df05376efcf60:0">You tell curl to read more command-line options from a specific file with the -K/--config option, like this:</span>

</span>

</span> curl -K cmdline.txt http://example.com<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="55c523746e60469da8cebc9725b3b2a8">

<span data-offset-key="55c523746e60469da8cebc9725b3b2a8:0">…and in the </span>

<span data-offset-key="55c523746e60469da8cebc9725b3b2a8:1">`cmdline.txt`</span>

<span data-offset-key="55c523746e60469da8cebc9725b3b2a8:2"> file (which, of course, can use any file name you please) you enter each command line per line:</span>

</span>

</span> # this is a comment, we ask to follow redirects--location# ask to do a HEAD request--head<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ec4e1392e9034621a4f1c444f81c653d">

<span data-offset-key="ec4e1392e9034621a4f1c444f81c653d:0">The config file accepts both short and long options, exactly as you would write them on a command line. As a special extra feature, it also allows you to write the long format of the options without the leading two dashes to make it easier to read. Using that style, the config file shown above can alternatively be written as:</span>

</span>

</span> # this is a comment, we ask to follow redirectslocation# ask to do a HEAD requesthead<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="034b9016e8f8435a8dbd67f2daefb113">

<span data-offset-key="034b9016e8f8435a8dbd67f2daefb113:0">Command line options that take an argument must have its argument provided on the same line as the option. For example changing the User-Agent HTTP header can be done with</span>

</span>

</span> user-agent "Everything-is-an-agent"<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8a79a922b8ac430587aaa9d359db3d0f">

<span data-offset-key="8a79a922b8ac430587aaa9d359db3d0f:0">To allow the config files to look even more like a true config file, it also allows you to use '=' or ':' between the option and its argument. As you see above it is not necessary, but some like the clarity it offers. Setting the user-agent option again:</span>

</span>

</span> user-agent = "Everything-is-an-agent"<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c01dbdb22f894bc3918d02b07691279d">

<span data-offset-key="c01dbdb22f894bc3918d02b07691279d:0">The argument to an option can be specified without double quotes and then curl will treat the next space or newline as the end of the argument. So if you want to provide an argument with embedded spaces you must use double quotes.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b41dd62683be444c99602bd4f1acba0e">

<span data-offset-key="b41dd62683be444c99602bd4f1acba0e:0">The user agent string example we have used above has no white spaces and therefore it can also be provided without the quotes like:</span>

</span>

</span> user-agent = Everything-is-an-agent<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="88159985804f415faa8b766e8d34a5a2">

<span data-offset-key="88159985804f415faa8b766e8d34a5a2:0">Finally, if you want to provide a URL in a config file, you must do that the </span>

<span data-offset-key="88159985804f415faa8b766e8d34a5a2:1">`--url`</span>

<span data-offset-key="88159985804f415faa8b766e8d34a5a2:2"> way, or just with </span>

<span data-offset-key="88159985804f415faa8b766e8d34a5a2:3">`url`</span>

<span data-offset-key="88159985804f415faa8b766e8d34a5a2:4">, and not like on the command line where everything that is not an option is assumed to be a URL. So you provide a URL for curl like this:</span>

</span>

</span> url = "http://example.com"<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="9ffd35b685d445f19e1571f8664f08f4">

<span data-offset-key="9ffd35b685d445f19e1571f8664f08f4:0">Default config file</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="613feb6727e44569b21bb8b074cd2705">

<span data-offset-key="613feb6727e44569b21bb8b074cd2705:0">When curl is invoked, it always (unless </span>

<span data-offset-key="613feb6727e44569b21bb8b074cd2705:1">`-q`</span>

<span data-offset-key="613feb6727e44569b21bb8b074cd2705:2"> is used) checks for a default config file and uses it if found. The file name it checks for is </span>

<span data-offset-key="613feb6727e44569b21bb8b074cd2705:3">`.curlrc`</span>

<span data-offset-key="613feb6727e44569b21bb8b074cd2705:4"> on Unix-like systems and </span>

<span data-offset-key="613feb6727e44569b21bb8b074cd2705:5">`_curlrc`</span>

<span data-offset-key="613feb6727e44569b21bb8b074cd2705:6"> on Windows.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="af0a646288eb44668f90501d6563cc80">

<span data-offset-key="af0a646288eb44668f90501d6563cc80:0">The default config file is checked for in the following places in this order:</span>

</span>

</span>1. <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="3976386444274470a7013a631e604e3b">

<span data-offset-key="3976386444274470a7013a631e604e3b:0">curl tries to find the "home directory": It first checks for the CURL_HOME and then the HOME environment variables. Failing that, it uses </span>

<span data-offset-key="3976386444274470a7013a631e604e3b:1">`getpwuid()`</span>

<span data-offset-key="3976386444274470a7013a631e604e3b:2"> on Unix-like systems (which returns the home directory given the current user in your system). On Windows, it then checks for the APPDATA variable, or as a last resort the '%USERPROFILE%\\Application Data'.</span>

</span>

</span>2. <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="06dc7477c79349ac88124deaa8d2e908">

<span data-offset-key="06dc7477c79349ac88124deaa8d2e908:0">On Windows, if there is no \_curlrc file in the home directory, it checks for one in the same directory the curl executable is placed. On Unix-like systems, it will simply try to load .curlrc from the determined home directory.</span>

</span>

</span>

<a href="listopts.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">List options</span>

<a href="passwords.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Passwords</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 12 months ago</span>
