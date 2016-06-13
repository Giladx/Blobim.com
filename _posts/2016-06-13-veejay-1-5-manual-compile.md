---
ID: 993
post_title: Veejay 1.5 manual compile
author: admin
post_date: 2016-06-13 00:05:48
post_excerpt: ""
layout: post
permalink: >
  http://blobim.com/index.php/2016/06/13/veejay-1-5-manual-compile/
published: true
---
VEEJAY 1.5 MANUAL COMPILE __ TESTED ON LUBUNTU 14.04

*First - Get all the dependencies

the working ffmpeg version:

you@linux:~$ sudo apt-add-repository ppa:kirillshkrogalev/ffmpeg-next

you@linux:~$ sudo apt-get update

you@linux:~$ sudo apt-get install ffmpeg ffmpeg2theora git autoconf automake libtool m4 gcc libjpeg62-dev libswscale-dev libavutil-dev libavcodec-dev libavformat-dev libx11-dev gtk-2.0-dev libxml2-dev libsdl1.2-dev libjack0 libjack-dev jackd1 libgmic-dev libglade2-dev libqrencode-dev libqrencode3 liblo-dev liblo-tools libunwind8 libunwind8-dev libdirectfb-bin libdirectfb-dev

**Next - get the git

you@linux:~$ git clone git://code.dyne.org/veejay.git veejay-git

you@linux:~$ cd veejay-git

you@linux:~/veejay-git$ git tag

***Now compile it

SERVER

you@linux:~$ cd veejay-git/veejay-current/

you@linux:~/veejay-git/veejay-current$ cd veejay-server

you@linux:~/veejay-git/veejay-current/veejay-server$ sh autogen.sh

you@linux:~/veejay-git/veejay-current/veejay-server$ ./configure

you@linux:~/veejay-git/veejay-current/veejay-server$ make

you@linux:~/veejay-git/veejay-current/veejay-server$ sudo make install

you@linux:~/veejay-git/veejay-current/veejay-server$ sudo ldconfig

CLIENT

you@linux:~/veejay-git/veejay-current$ cd veejay-client

you@linux:~/veejay-git/veejay-current/veejay-client$ sh autogen.sh

you@linux:~/veejay-git/veejay-current/veejay-client$ ./configure

you@linux:~/veejay-git/veejay-current/veejay-client$ make

you@linux:~/veejay-git/veejay-current/veejay-client$ sudo make install

you@linux:~/veejay-git/veejay-current/veejay-client$ sudo ldconfig

VIMS

you@linux:~/veejay-git/veejay-current$ cd sendVIMS

you@linux:~/veejay-git/veejay-current/sendVIMS$ ./configure

you@linux:~/veejay-git/veejay-current/sendVIMS$ make

you@linux:~/veejay-git/veejay-current/sendVIMS$ sudo make install

OTHER STUFF

Use the same routine to install the plugins &amp; utils

dont forget to -- sudo ldconfig

$ echo "goodluck &amp;&amp; enjoy :)"
*to install themes just cd the dir and run sudo ./INSTALL

GIL@DX

gilad@blobim.com blobim.com