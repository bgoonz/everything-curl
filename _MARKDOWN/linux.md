<a href="linux.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca--navButtonOpened-6a88552e">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Linux</span>
</a>
<a href="windows.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">Windows</span>
</a>
<a href="macos.html" class="navButton-94f2579c--pageItemWithChildrenNested-2c5d8183--navButtonClickable-161b88ca">
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1--navButtonLabel-14a4968f">macOS</span>
</a>
# <span class="text-4505230f--DisplayH900-bfb998fa--textContentFamily-49a318e1">Linux</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--UIH300-2063425d--textUIFamily-5ebd8e40--text-8ee2c8b2">
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="d769d15f4a654771846cc59f45ea7901">
<span data-offset-key="d769d15f4a654771846cc59f45ea7901:0">Linux distributions come with "packager managers" that let you install software that they offer. Most Linux distributions offer curl and libcurl to be installed if they are not installed by default.</span>
</span>
</span>
<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="857547443de043a48046d27c6ac79a87">
<span data-offset-key="857547443de043a48046d27c6ac79a87:0">Ubuntu and Debian</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="b223a33a833147fd8575e95fbd1ac81d">
<span data-offset-key="b223a33a833147fd8575e95fbd1ac81d:0">`apt`</span>
<span data-offset-key="b223a33a833147fd8575e95fbd1ac81d:1"> is a tool to install prebuilt packages on Debian Linux and Ubuntu Linux distributions and derivatives.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="c8e747be066a49e0899fbbe5d22f7efa">
<span data-offset-key="c8e747be066a49e0899fbbe5d22f7efa:0">To install the curl command-line tool, you usually just</span>
</span>
</span>    apt install curl<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="92a926e3313e45fa81c244bd9331f228">
<span data-offset-key="92a926e3313e45fa81c244bd9331f228:0">…and that then makes sure the dependencies are installed and usually libcurl is then also installed as an individual package.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="01c14da4f1c6493695df93fe7d535f20">
<span data-offset-key="01c14da4f1c6493695df93fe7d535f20:0">If you want to build applications against libcurl, you need a development package installed to get the include headers and some additional documentation, etc. You can then select a libcurl with the TLS backend you prefer:</span>
</span>
</span>    apt install libcurl4-openssl-dev<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="4b1cca6ad8f44286abac2fab0eeded55">
<span data-offset-key="4b1cca6ad8f44286abac2fab0eeded55:0">or</span>
</span>
</span>    apt install libcurl4-nss-dev<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="e858730b86e54887b9a0f6e0b85d7862">
<span data-offset-key="e858730b86e54887b9a0f6e0b85d7862:0">or</span>
</span>
</span>    apt install libcurl4-gnutls-dev<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="a319e894f41d4e388e9bf0150622e16c">
<span data-offset-key="a319e894f41d4e388e9bf0150622e16c:0">Redhat and Centos</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="dc8997810f5248e0b6576ab6a4b0248e">
<span data-offset-key="dc8997810f5248e0b6576ab6a4b0248e:0">With Redhat Linux and CentOS Linux derivatives, you use </span>
<span data-offset-key="dc8997810f5248e0b6576ab6a4b0248e:1">`yum`</span>
<span data-offset-key="dc8997810f5248e0b6576ab6a4b0248e:2"> to install packages. Install the command-line tool with:</span>
</span>
</span>    yum install curl<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="b061946795f34b48b19df68d6d59ed66">
<span data-offset-key="b061946795f34b48b19df68d6d59ed66:0">You install the libcurl development package (with include files and some docs, etc.) with this:</span>
</span>
</span>    yum install libcurl-devel<span class="text-4505230f--HeadingH600-23f228db--textContentFamily-49a318e1">
<span data-key="b4f844d711dd4aea816a6d39524cc7e7">
<span data-offset-key="b4f844d711dd4aea816a6d39524cc7e7:0">nix</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="8bd1c03dc6a747a1be82cf33ca08e71d">
<span data-offset-key="8bd1c03dc6a747a1be82cf33ca08e71d:0">
<span data-slate-zero-width="z">​</span>
</span>
</span>
<a href="https://nixos.org/nix/" class="link-a079aa82--primary-53a25e66--link-faf6c434">
<span data-key="280f98dd26e049e8873741a4153addb2">
<span data-offset-key="280f98dd26e049e8873741a4153addb2:0">Nix</span>
</span>
</a>
<span data-key="901f312e5b664bef82bc1b34994acbd1">
<span data-offset-key="901f312e5b664bef82bc1b34994acbd1:0"> is a package manager default to the NixOS distribution, but it can also be used on any Linux distribution.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="e513324366324aefae5ec996ed508484">
<span data-offset-key="e513324366324aefae5ec996ed508484:0">In order to install command-line tool:</span>
</span>
</span>    nix-env -i curl<span class="text-4505230f--HeadingH700-04e1a2a3--textContentFamily-49a318e1">
<span data-key="730476474069464ba012acb46a8f0e8b">
<span data-offset-key="730476474069464ba012acb46a8f0e8b:0">Arch Linux</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="a3c3da89777c4cb2aae5f86636540a96">
<span data-offset-key="a3c3da89777c4cb2aae5f86636540a96:0">curl is located in the core repository of Arch Linux. This means it should be installed automatically if you follow the normal installation procedure.</span>
</span>
</span>
<span class="text-4505230f--TextH400-3033861f--textContentFamily-49a318e1">
<span data-key="95d3a34e31a34268ad41e68e0af61e4e">
<span data-offset-key="95d3a34e31a34268ad41e68e0af61e4e:0">If curl is not installed, Arch Linux uses </span>
<span data-offset-key="95d3a34e31a34268ad41e68e0af61e4e:1">`pacman`</span>
<span data-offset-key="95d3a34e31a34268ad41e68e0af61e4e:2"> to install packages:</span>
</span>
</span>    pacman -S curl<a href="../get.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardPrevious-56a5e674">
</a>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Previous</span>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Get curl</span>
<a href="windows.html" class="reset-3c756112--card-6570f064--whiteCard-fff091a4--cardNext-19241c42">
</a>
<span class="text-4505230f--UIH400-4e41e82a--textContentFamily-49a318e1">Windows</span>
<span class="text-4505230f--TextH200-a3425406--textContentFamily-49a318e1">Last updated 8 months ago</span>
<span class="text-4505230f--InfoH100-1e92e1d1--textContentFamily-49a318e1">Contents</span>
<a href="linux.html#ubuntu-and-debian" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Ubuntu and Debian</span>
</span>
<a href="linux.html#redhat-and-centos" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Redhat and Centos</span>
</span>
<a href="linux.html#nix" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1--pageTocLinkH2-2294976c">nix</span>
</span>
<a href="linux.html#arch-linux" class="reset-3c756112--menuItem-aa02f6ec--menuItemLight-757d5235--menuItemInline-173bdf97--pageTocItem-f4427024">
</a>
<span class="text-4505230f--UIH300-2063425d--textContentFamily-49a318e1">
<span class="text-4505230f--UIH200-50ead35f--textContentFamily-49a318e1">Arch Linux</span>
</span>
