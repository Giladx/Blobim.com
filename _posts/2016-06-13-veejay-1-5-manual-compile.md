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

you@linux:~$ <code>sudo apt-add-repository ppa:kirillshkrogalev/ffmpeg-next</code>

you@linux:~$ <code>sudo apt-get update

you@linux:~$ <code>sudo apt-get install ffmpeg ffmpeg2theora git autoconf automake libtool m4 gcc libjpeg62-dev libswscale-dev libavutil-dev libavcodec-dev libavformat-dev libx11-dev gtk-2.0-dev libxml2-dev libsdl1.2-dev libjack0 libjack-dev jackd1 libgmic-dev libglade2-dev libqrencode-dev libqrencode3 liblo-dev liblo-tools libunwind8 libunwind8-dev</code> libdirectfb-bin libdirectfb-dev

**Next - get the git

you@linux:~$ <code>git clone git://code.dyne.org/veejay.git veejay-git</code>

you@linux:~$ <code>cd veejay-git</code>

you@linux:~/veejay-git$ <code>git tag</code>

***Now compile it

SERVER

you@linux:~$ <code>cd veejay-git/veejay-current/</code>

you@linux:~/veejay-git/veejay-current$ <code>cd veejay-server</code>

you@linux:~/veejay-git/veejay-current/veejay-server$ <code>sh autogen.sh</code>

you@linux:~/veejay-git/veejay-current/veejay-server$ <code>./configure</code>

you@linux:~/veejay-git/veejay-current/veejay-server$ <code>make</code>

you@linux:~/veejay-git/veejay-current/veejay-server$ <code>sudo make install</code>

you@linux:~/veejay-git/veejay-current/veejay-server$ <code>sudo ldconfig</code>

CLIENT

you@linux:~/veejay-git/veejay-current$ <code>cd veejay-client</code>

you@linux:~/veejay-git/veejay-current/veejay-client$ <code>sh autogen.sh</code>

you@linux:~/veejay-git/veejay-current/veejay-client$ <code>./configure</code>

you@linux:~/veejay-git/veejay-current/veejay-client$ <code>make</code>

you@linux:~/veejay-git/veejay-current/veejay-client$ <code>sudo make install</code>

you@linux:~/veejay-git/veejay-current/veejay-client$ <code>sudo ldconfig</code>

VIMS

you@linux:~/veejay-git/veejay-current$ <code>cd sendVIMS</code>

you@linux:~/veejay-git/veejay-current/sendVIMS$ <code>./configure</code>

you@linux:~/veejay-git/veejay-current/sendVIMS$ <code>make</code>

you@linux:~/veejay-git/veejay-current/sendVIMS$ <code>sudo make install</code>

OTHER STUFF

Use the same routine to install the plugins &amp; utils

dont forget to -- <code>sudo ldconfig

$ <code>echo "goodluck &amp;&amp; enjoy :)"</code>
*to install themes just cd the dir and run <code>sudo ./INSTALL</code>

GIL@DX

gilad@blobim.com blobim.com