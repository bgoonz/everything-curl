# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Code style</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="25d55aa9f89f4f929705fe0fe9eb33a5">

<span data-offset-key="25d55aa9f89f4f929705fe0fe9eb33a5:0">Source code that has a common style is easier to read than code that uses different styles in different places. It helps making the code feel like one continuous code base. Easy-to-read is a important property of code and helps make it easier to review when new things are added and it helps debugging code when developers are trying to figure out why things go wrong. A unified style is more important than individual contributors having their own personal tastes satisfied.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="8e5fe42a8b9341f386ee3ca5dbee321c">

<span data-offset-key="8e5fe42a8b9341f386ee3ca5dbee321c:0">Our C code has a few style rules. Most of them are verified and upheld by the lib/checksrc.pl script. Invoked with </span>

<span data-offset-key="8e5fe42a8b9341f386ee3ca5dbee321c:1">`make checksrc`</span>

<span data-offset-key="8e5fe42a8b9341f386ee3ca5dbee321c:2"> or even by default by the build system when built after </span>

<span data-offset-key="8e5fe42a8b9341f386ee3ca5dbee321c:3">`./configure --enable-debug`</span>

<span data-offset-key="8e5fe42a8b9341f386ee3ca5dbee321c:4"> has been used.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="984cb38215164b4b981c6908578ed316">

<span data-offset-key="984cb38215164b4b981c6908578ed316:0">It is normally not a problem for anyone to follow the guidelines as you just need to copy the style already used in the source code, and there are no particularly unusual rules in our set of rules.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4473984865f5408a9237b2e8a502218f">

<span data-offset-key="4473984865f5408a9237b2e8a502218f:0">We also work hard on writing code that is warning-free on all the major platforms and in general on as many platforms as possible. Code that obviously will cause warnings will not be accepted as-is.</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="4968b044bd2f40e897fdba4352f5b4cd">

<span data-offset-key="4968b044bd2f40e897fdba4352f5b4cd:0">Some of the rules that you will not be allowed to break are:</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="9edfac33e5d24f939167fa6146b41e47">

<span data-offset-key="9edfac33e5d24f939167fa6146b41e47:0">Indentation</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="f0118ad24a0d46f7af34653634a121e9">

<span data-offset-key="f0118ad24a0d46f7af34653634a121e9:0">We use only spaces for indentation, never TABs. We use two spaces for each new open brace.</span>

</span>

</span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="a9d73783d31942de901de47f3127d27b">

<span data-offset-key="a9d73783d31942de901de47f3127d27b:0">Comments</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="43146effd6b4461aa87a67ef13269005">

<span data-offset-key="43146effd6b4461aa87a67ef13269005:0">Since we write C89 code, // are not allowed. They were not introduced in the C standard until C99. We use only /\* and \*/ comments:</span>

</span>

</span>

    /* this is a comment */

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="9d57ac9ed4de44b7ade7a655ab477fc8">

<span data-offset-key="9d57ac9ed4de44b7ade7a655ab477fc8:0">Long lines</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="a04589b9d57b4c539350a0ab7f3323fb">

<span data-offset-key="a04589b9d57b4c539350a0ab7f3323fb:0">Source code in curl may never be wider than 80 columns. There are two reasons for maintaining this even in the modern era of large and high resolution screens:</span>

</span>

</span>

1.  <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
    <span data-key="631b2cd5880e4d06927598e30f96695b">
    <span data-offset-key="631b2cd5880e4d06927598e30f96695b:0">Narrower columns are easier to read than wide ones. There's a reason newspapers have used columns for decades or centuries.</span>
    </span>
    </span>

2.  <span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
    <span data-key="4f40d97f5250426d877c3fed890e88aa">
    <span data-offset-key="4f40d97f5250426d877c3fed890e88aa:0">Narrower columns allow developers to more easily view multiple pieces of code next to each other in different windows. I often have two or three source code windows next to each other on the same screen, as well as multiple terminal and debugging windows.</span>
    </span>
    </span>

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="b5531b504fec4e269cdbe292b12b4221">

<span data-offset-key="b5531b504fec4e269cdbe292b12b4221:0">Open brace on the same line</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="e26e8ad7f61e4fd9b61d1de9636a99e6">

<span data-offset-key="e26e8ad7f61e4fd9b61d1de9636a99e6:0">In if/while/do/for expressions, we write the open brace on the same line as the keyword and we then set the closing brace on the same indentation level as the initial keyword. Like this:</span>

</span>

</span>

    if(age < 40) {  /* clearly a youngster */}

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="94487d804a2e4649a95cbef4cba35ab2">

<span data-offset-key="94487d804a2e4649a95cbef4cba35ab2:0">else on the following line</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="6d39d6f6d3b44163b97f7806618d2b54">

<span data-offset-key="6d39d6f6d3b44163b97f7806618d2b54:0">When adding an </span>

<span data-offset-key="6d39d6f6d3b44163b97f7806618d2b54:1">`else`</span>

<span data-offset-key="6d39d6f6d3b44163b97f7806618d2b54:2"> clause to a conditional expression using braces, we add it on a new line after the closing brace. Like this:</span>

</span>

</span>

    if(age < 40) {  /* clearly a youngster */}else {  /* probably intelligent */}

<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">

<span data-key="74dc8b9af675470484cf4e3609b8c3ee">

<span data-offset-key="74dc8b9af675470484cf4e3609b8c3ee:0">No space before parentheses</span>

</span>

</span>

<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">

<span data-key="9878483da2a048e0818280a839b074e4">

<span data-offset-key="9878483da2a048e0818280a839b074e4:0">When writing expressions using if/while/do/for, there shall be no space between the keyword and the open parenthesis. Like this:</span>

</span>

</span>

    while(1) {  /* loop forever */}

<a href="options.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">

</a>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Handling build options</span>

<a href="contributing.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">

</a>

<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Contributing</span>

<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 8 months ago</span>

<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>

<a href="style.html#indentation" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Indentation</span>

</span>

<a href="style.html#comments" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Comments</span>

</span>

<a href="style.html#long-lines" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Long lines</span>

</span>

<a href="style.html#open-brace-on-the-same-line" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Open brace on the same line</span>

</span>

<a href="style.html#else-on-the-following-line" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">else on the following line</span>

</span>

<a href="style.html#no-space-before-parentheses" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">

</a>

<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">

<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">No space before parentheses</span>

</span>
