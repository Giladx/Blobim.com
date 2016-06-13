---
ID: 996
post_title: 'how to compile VEEJAY 1.5  on  lubuntu 14.04'
author: admin
post_date: 2016-06-13 00:18:45
post_excerpt: ""
layout: page
permalink: >
  http://blobim.com/index.php/veejay-1-5-lubuntu-14-04/
published: true
---
<strong>VEEJAY 1.5 MANUAL COMPILE __ TESTED ON LUBUNTU 14.04</strong>

(I belive this will work on any ubuntu 14.04 based system)

&nbsp;

<strong>*First - Get all the dependencies</strong>

<strong>working ffmpeg ppa:</strong>

<code>sudo apt-add-repository ppa:kirillshkrogalev/ffmpeg-next</code>

<code>sudo apt-get update</code>

<code>sudo apt-get install ffmpeg ffmpeg2theora git autoconf automake libtool m4 gcc libjpeg62-dev libswscale-dev libavutil-dev libavcodec-dev libavformat-dev libx11-dev gtk-2.0-dev libxml2-dev libsdl1.2-dev libjack0 libjack-dev jackd1 libgmic-dev libglade2-dev libqrencode-dev libqrencode3 liblo-dev liblo-tools libunwind8 libunwind8-dev libdirectfb-bin libdirectfb-dev</code>

&nbsp;

<strong>**Next - get the git</strong>

<code>git clone git://code.dyne.org/veejay.git veejay-git</code>

<code>cd veejay-git</code>

<code>git tag</code>

<code>cd veejay-current</code>

&nbsp;

<strong>***Now compile it</strong>

&nbsp;

<strong>SERVER</strong>

<code>cd veejay-server</code>

<code>sh autogen.sh</code>

<code>./configure</code>

<code>make</code>

<code>sudo make install
</code>
<code>sudo ldconfig</code>

&nbsp;

<strong>CLIENT</strong>

<code>cd veejay-client</code>

<code>sh autogen.sh</code>

<code>./configure</code>

<code>make</code>

<code>sudo make install</code>

<code>sudo ldconfig</code>

&nbsp;

<strong>VIMS</strong>

<code>cd sendVIMS</code>

<code>./configure</code>

<code>make</code>

<code>sudo make install</code>

&nbsp;

<strong>OTHER STUFF</strong>

Use the same routine to install the plugins &amp; utils

dont forget to -- sudo ldconfig

<code>$ echo "goodluck &amp;&amp; enjoy :)"</code>
*to install themes just cd the dir and run <code>sudo ./INSTALL</code>

<strong>GIL@DX</strong>

gilad@blobim.com blobim.com