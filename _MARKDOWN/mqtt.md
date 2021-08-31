<a href="mqtt.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">

</a>

</a>

# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">MQTT</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="123c8bf295504fa08e27b702adfd3236">

<span data-offset-key="123c8bf295504fa08e27b702adfd3236:0">A plain "GET" subscribes to the topic and prints all published messages. Doing a "POST" publishes the post data to the topic and exits.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c76cd45a8159476f92ee54afeaeecd96">

<span data-offset-key="c76cd45a8159476f92ee54afeaeecd96:0">Subscribe to the temperature in the "home/bedroom" subject published by example.com:</span>

</span>

</span>    curl mqtt://example.com/home/bedroom/temp<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="c57386aa40d74903986d4df8a1a3c6ad">

<span data-offset-key="c57386aa40d74903986d4df8a1a3c6ad:0">Send the value '75' to the "home/bedroom/dimmer" subject hosted by the example.com server:</span>

</span>

</span>    curl -d 75 mqtt://example.com/home/bedroom/dimmer<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="6602bbb617244738bd0f5367e739fb77">

<span data-offset-key="6602bbb617244738bd0f5367e739fb77:0">What does curl deliver as a response to a subscribe</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="1f081fba4c6e44f0b710fe3896ce2e0d">

<span data-offset-key="1f081fba4c6e44f0b710fe3896ce2e0d:0">It outputs two bytes topic length (MSB | LSB), the topic followed by the payload.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="235e3011aef4405b817f331c5995ca55">

<span data-offset-key="235e3011aef4405b817f331c5995ca55:0">Caveats</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="b3aa21f583e541afad16868a2084c7e4">

<span data-offset-key="b3aa21f583e541afad16868a2084c7e4:0">Remaining limitations in curl's MQTT support as of September 2020:</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="02768d92df56454fa3552411d33b231f">

<span data-offset-key="02768d92df56454fa3552411d33b231f:0">No username support</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="31acea37ba0943d382350203fddf1d1e">

<span data-offset-key="31acea37ba0943d382350203fddf1d1e:0">Only QoS level 0 is implemented for publish</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="0e904f3fc7b3435f84e252169b9a2421">

<span data-offset-key="0e904f3fc7b3435f84e252169b9a2421:0">No way to set retain flag for publish</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="2673be83417049b6948a048ceee41250">

<span data-offset-key="2673be83417049b6948a048ceee41250:0">No username/password support</span>

</span>

</span>- <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="ebc7d5fa1b024b39acf3384622b0fcdb">

<span data-offset-key="ebc7d5fa1b024b39acf3384622b0fcdb:0">No TLS (mqtts) support</span>

</span>

</span>

<a href="smtp.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Sending email</span>

<a href="telnet.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">TELNET</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 11 months ago</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="mqtt.html#what-does-curl-deliver-as-a-response-to-a-subscribe" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">What does curl deliver as a response to a subscribe</span>

</span>

<a href="mqtt.html#caveats" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Caveats</span>

</span>
