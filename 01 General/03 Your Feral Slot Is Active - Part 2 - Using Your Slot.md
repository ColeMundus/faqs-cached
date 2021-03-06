<h1>Your Feral Slot Is Active - Part 2 - Using Your Slot</h1>

        
Your server is a remote device. What does this mean? It means that your Feral slot is totally separate from your physical location. Like a computer in another person&#x27;s house. This is often where people get confused, regarding what is done on their home devices and what the server does. I will do my best to make it as easy to understand as possible, so that at the end, hopefully, you have a clear picture of how this whole seed slot thing works. <br>
<br>
Let us look at the difference in physical locations.<br>
<br>
<img src="https://raw.github.com/feralhosting/feralfilehosting/master/Feral Wiki/General/Your Feral slot is active - Part 2 - Using your slot/01 location 1.png"><br>
<br>
When you buy a slot from Feral it will be activated and created on a server in the carrier-neutral Interxion data centre in Netherlands.<br>
<br>
No matter where in the world you are, you will be connecting to this location when you directly access your slot&#x27;s features. <br>
<br>
All <em>outgoing</em> traffic from your Feral Slot originates from this Netherlands location.<br>
<br>
<img src="https://raw.github.com/feralhosting/feralfilehosting/master/Feral Wiki/General/Your Feral slot is active - Part 2 - Using your slot/01 location 2.png"><br>
<br>
So how do I do stuff? Well, it is actually quite easy once you understand the basic concepts. Your slot is another device in another place and Feral&#x27;s set-up provides you with the tools and services you need to manage it remotely.<br>
<br>
<h2>Web Gui</h2><br>
A Web Gui is provided for ruTorrent, Deluge and Transmission to remotely control the applications running on the server.<br>
<br>
So how do I get torrents downloading and uploading on my slot, and not on my home devices?<br>
<br>
First you would need to have installed one or more of the applications discussed in <a href="https://www.feralhosting.com/faq/view?question=134">Part 1</a> of this FAQ.<br>
<br>
Then you would access your slot&#x27;s Web Gui from your local devices using a Web browser like Firefox.<br>
<br>
You would usually download a torrent file directly to your local machine and then upload it&#x2F;open it in the Web Gui of your choice. The Web Gui will then communicate this to the running processes on your server. The running processes, for example rTorrent, will then communicate with trackers and peers directly from the server.<br>
<br>
Here is a breakdown of using a Web Gui.<br>
<br>
<strong>1:</strong> Visit a torrent site and find a torrent file or a magnet link<br>
<strong>2:</strong> Download and save the torrent file to your local device (do not open it directly with another program, like uTorrent) or copy the magnet URL<br>
<strong>3:</strong> Visit the Web Gui of the application you installed, for example ruTorrent.<br>
<strong>4:</strong> Follow the Steps shown below to add this torrent in the Web Gui so that it is passed to rTorrent running on your slot.<br>
<br>
<strong>Important note:</strong> This is where people often get confused. You will need to download torrent files to your device first and then upload them to the Web Gui. <br>
<br>
There are ways to bypass this step, of first downloading to your local machine, such as using: <br>
<br>
<a href="https://addons.mozilla.org/en-us/firefox/addon/bittorrent-webui-120685/">Browser addons for Firefox</a> <br>
<a href="https://www.feralhosting.com/faq/view?question=146">Extension for Chrome</a><br>
<a href="https://www.feralhosting.com/faq/view?question=76">Deluge Thin Client</a><br>
<a href="https://www.feralhosting.com/faq/view?question=4">Transmission Remote Gui</a><br>
<br>
These methods are not covered in this FAQ but once you have the idea you can make use of them. For this FAQ we are doing things in the default way as per the default set-up.<br>
<br>
Here is a brief overview of how using the Web Gui works so that you can better understand what it means to you and how it works.<br>
<br>
<img src="https://raw.github.com/feralhosting/feralfilehosting/master/Feral Wiki/General/Your Feral slot is active - Part 2 - Using your slot/02 webgui.png"><br>
<br>
As the image shows, the Web Gui interacts with the processes running on the server and that allows you to do things like add torrents and magnet links. The running processes will then deal directly with your tracker and peers.<br>
<br>
This means you can turn off your PC and it will not affect the running processes such as rTorrent or Deluge. They run on your server and you are only interacting with them using the Web Gui. Closing the Web Gui or turning off you PC will not stop theses programs from working.<br>
<br>
<h2>ruTorrent Web Gui</h2><br>
<strong>Important note:</strong> ruTorrent (Gui) is blamed for causing rTorrent (the actual program) to crash and become unstable when dealing with large number of active torrents, in the range 1500 to 5000. In this case it is recommended to only use rTorrent (SSH) for managing your torrents. This means you should avoid using the Gui with large volumes of files and active torrents.<br>
<br>
<a href="https://github.com/Novik/ruTorrent">ruTorrent</a> is a front-end for the popular Bittorrent client <a href="https://github.com/rakshasa/rtorrent">rTorrent</a>. It uses the power of the rTorrent back-end combined with the Web interface from utorrent for one powerful combination. rTorrent is a very powerful client, and comes preconfigured with settings. The default settings work fine so you should only troubleshoot by changing the settings as a last resort. ruTorrent comes with a number of plug-ins installed that expand what ruTorrent can do. rTorrent without a Web Gui can handle thousands of torrents and is highly stable.<br>
<br>
<img src="https://raw.github.com/feralhosting/feralfilehosting/master/Feral Wiki/General/Your Feral slot is active - Part 2 - Using your slot/03 rutorrent 1.png"><br>
<br>
In the navigation menu on the top left of ruTorrent click on the Globe.<br>
<br>
<img src="https://raw.github.com/feralhosting/feralfilehosting/master/Feral Wiki/General/Your Feral slot is active - Part 2 - Using your slot/03 rutorrent 2.png"><br>
<br>
Now you will get this window. Here you browse for the torrent files you downloaded to your local machine from your Torrent site.<br>
<br>
<strong>Related tutorial:</strong> <a href="https://www.feralhosting.com/faq/view?question=202">Selecting an rTorrent version</a><br>
<br>
<strong>Related tutorial:</strong> <a href="https://www.feralhosting.com/faq/view?question=158">Restarting - rTorrent - Deluge - Transmission - MySQL</a><br>
<br>
<strong>Related tutorial:</strong> <a href="https://www.feralhosting.com/faq/view?question=100">ruTorrent - Troubleshooting</a><br>
<br>
<strong>Related tutorial:</strong> <a href="https://www.feralhosting.com/faq/view?question=2">Using rTorrent (Advanced) and Troubleshooting Common Errors</a> <br>
<br>
<strong>Related tutorial:</strong> <a href="https://www.feralhosting.com/faq/view?question=126">Feralstats plugin for ruTorrent</a><br>
<br>
<h2>Deluge Web Gui</h2><br>
Deluge is a fully fledged BitTorrent client that aggressively downloads content from peers. It provides it&#x27;s own Web interface to control access. Deluge is the other client we recommend. Deluge is great for initially seeding your downloads or uploads because of its peering strategy. For seeding, Deluge is a great choice, however, its limited to 1000 open files (most torrents contain multiple files) therefore it is not well suited to seeding many torrents, about 250 torrents (this is an average of 4 files per torrent). <br>
<br>
<strong>Important Note:</strong> Plug ins do not work with the Web Gui, you will need to use the <a href="https://www.feralhosting.com/faq/view?question=76">Deluge Thin Client</a>.<br>
<br>
In the Deluge Web Gui you must first connect to the Deluge daemon.<br>
<br>
<img src="https://raw.github.com/feralhosting/feralfilehosting/master/Feral Wiki/General/Your Feral slot is active - Part 2 - Using your slot/04 deluge 1.png"><br>
<br>
Once you have done that you will be able to control Deluge and start uploading or downloading.<br>
<br>
Click on &quot;Add&quot; in the navigation bar.<br>
<br>
<img src="https://raw.github.com/feralhosting/feralfilehosting/master/Feral Wiki/General/Your Feral slot is active - Part 2 - Using your slot/04 deluge 2.png"><br>
<br>
Now select the type of torrent, file or magnet URL you would like to upload.<br>
<br>
<img src="https://raw.github.com/feralhosting/feralfilehosting/master/Feral Wiki/General/Your Feral slot is active - Part 2 - Using your slot/04 deluge 3.png"><br>
<br>
<strong>Related tutorial:</strong> <a href="https://www.feralhosting.com/faq/view?question=158">Restarting - rTorrent - Deluge - Transmission - MySQL</a><br>
<br>
<strong>Related tutorial:</strong> <a href="https://www.feralhosting.com/faq/view?question=62">Troubleshooting Deluge</a><br>
<br>
<strong>Related tutorial:</strong> <a href="https://www.feralhosting.com/faq/view?question=76">Deluge Thin Client</a><br>
<br>
<h2>Transmission Web Gui</h2><br>
Transmission is a fast, easy, and free multi-platform BitTorrent client that comes with a Web interface. While not the preferred client of those offered, Transmission&#x27;s interface is simple and easy to understand. Transmission works well for low numbers of torrents, less than 100, and can be used at most private trackers. Please be aware, some trackers may not support Transmission or the version we use.&nbsp; <br>
<br>
In the Transmission Web Gui you click on the Folder icon to add a torrent or magnet link.<br>
<br>
<img src="https://raw.github.com/feralhosting/feralfilehosting/master/Feral Wiki/General/Your Feral slot is active - Part 2 - Using your slot/05 transmission 1.png"><br>
<br>
Now provide the file or URL of the torrent you wish to open.<br>
<br>
<img src="https://raw.github.com/feralhosting/feralfilehosting/master/Feral Wiki/General/Your Feral slot is active - Part 2 - Using your slot/05 transmission 2.png"><br>
<br>
<strong>Related tutorial:</strong> <a href="https://www.feralhosting.com/faq/view?question=158">Restarting - rTorrent - Deluge - Transmission - MySQL</a><br>
<br>
<strong>Related tutorial:</strong> <a href="https://www.feralhosting.com/faq/view?question=4">Transmission Remote Gui</a><br>
<br>
<h2>Remote Clients</h2><br>
You can also control some of the server software as if it was installed on your PC in some cases using these programs.<br>
<br>
<strong>ruTorrent and Deluge:</strong> you can run <a href="https://www.feralhosting.com/faq/view?question=81">Transdroid</a> (requires Java)<br>
<br>
<strong>Deluge only:</strong> you can also run the <a href="https://www.feralhosting.com/faq/view?question=76">Thin Client</a>. Recommended for Deluge, requires you install Deluge first using the Install Software link in your manager.<br>
<br>
<strong>Transmission only:</strong> you can also run <a href="https://www.feralhosting.com/faq/view?question=4">Transmission Remote Gui</a><br>
<br>
Here is a brief overview of how SSH works.<br>
<br>
<h2>SSH</h2><br>
SSH stands for <strong>Secure Shell</strong>, and is a command line interface to interact with your slot. You can move, copy, delete, archive and create files, among other things, on your slot through SSH. Learning the basics of SSH will save you time and help you be more efficient. SSH gives you control over the device as if you were controlling it locally. This means that you can send commands and control applications. SSH is a pretty powerful feature that will let you do cool things like install software and stuff, but that is covered in other FAQS. We recommend using the <a href="https://www.feralhosting.com/faq/view?question=12">SSH guide basics - PuTTy</a> FAQ to get started.<br>
<br>
Here is a brief overview of how using the SSH works so you can better understand what it means to you and when you might need to use it.<br>
<br>
<img src="https://raw.github.com/feralhosting/feralfilehosting/master/Feral Wiki/General/Your Feral slot is active - Part 2 - Using your slot/06 ssh.png"><br>
<br>
Using SSH is an important part of using your slot as it will give you a great deal of control and flexibility over managing it.<br>
<br>
<strong>Related tutorial:</strong>&nbsp; <a href="https://www.feralhosting.com/faq/view?question=12">SSH guide basics - PuTTy</a><br>
<br>
<strong>Related tutorial:</strong>&nbsp; <a href="https://www.feralhosting.com/faq/view?question=217">SSH guide basics - Mac</a><br>
<br>
<strong>Related tutorial:</strong>&nbsp; <a href="https://www.feralhosting.com/faq/view?question=13">Public Key Authentication for password-less login</a><br>
<br>
<h2>SSH Tunnels</h2><br>
All slots allow the user to connect using SSH and create something called an SSH Tunnel. This will allow you to <strong>selectively</strong> route all traffic from applications through your server.<br>
<br>
When using SSH tunnels you will use an SSH client like Putty to create a local SOCKS 5 proxy and then tell your applications to use this proxy to connect to the internet. Any program that has proxy settings can be use with an SSH tunnel.<br>
<br>
Though there are some technical differences between how an SSH tunnel and OpenVPN work the end result is pretty much the same. Except with an SSH tunnel you can create as many tunnels as you need, on different machines, whilst only routing what you need through the server and not everything that passes through your network adapter. This can be useful when you only want to route certain things, like utorrent.<br>
<br>
Here is a picture showing the basic concepts of using SSH tunnels with your slot.<br>
<br>
<img src="https://raw.github.com/feralhosting/feralfilehosting/master/Feral Wiki/General/Your Feral slot is active - Part 2 - Using your slot/07 sshtunnel.png"><br>
<br>
<strong>Related tutorial:</strong>&nbsp; <a href="https://www.feralhosting.com/faq/view?question=37">SSH tunnels basics - Putty and setting a Socks proxy</a><br>
<br>
<strong>Related tutorial:</strong>&nbsp; <a href="https://www.feralhosting.com/faq/view?question=79">SSH tunnels - MyEnTunnel 3.5 using Plink and setting a Socks proxy</a><br>
<br>
<strong>Related tutorial:</strong>&nbsp; <a href="https://www.feralhosting.com/faq/view?question=217">SSH guide basics - Mac</a><br>
<br>
<h2>OpenVPN</h2><br>
A VPN can help mask your identity, in the form of your ISP assigned IP address, when browsing, it does not alone make you completely anonymous in the way they are often marketed.<br>
<br>
There is also distinction between privacy and anonymity that is quite an important one.<br>
<br>
Privacy is nobody seeing what you do, but potentially knowing who you are.<br>
Privacy is a person’s right to control access to his or her personal information.<br>
<br>
Anonymity is nobody knowing who you are, but potentially seeing what you do.<br>
Anonymity is a condition in which an individual’s true identity is unknown.<br>
<br>
Traffic leaving and returning to the server behaves as normal. This means you should still use <code>https</code> where possible and maintain good browsing practices. A VPN does not wave a magical wand and make you a <a href="http://i.imgur.com/ZlUEvSU.jpg">super secret squirrel</a>.<br>
<br>
All slots can install OpenVPN Server so that users can use OpenVPN supporting software (clients) to route all their local traffic through their feral slot via the OpenVPN server.<br>
<br>
<strong>Important note:</strong> Each OpenVPN installation is limited to a <strong>single open connection</strong> at any one time. You cannot have multiple OpenVPN clients establish an open connection to your Feral OpenVPN server at the same time. So this means only one device behind a firewall&#x2F;router would be able to connect directly to and through the Feral slot OpenVPN server. Some routers will allow you to configure and connect to the OpenVPN server from directly within the router set-up allowing all users behind to connect via the Feral Slot OpenVPN server.<br>
<br>
OpenVPN is basically a way to have the benefits of LAN access from a remote location and it encrypts traffic at the driver level. In regards to the Feral set-up there are no particular benefits to using OpenVPN over using an SSH tunnel, except where special needs or requirements demand it. For example some applications do not support using a proxy, like rTorrent.<br>
<br>
An OpenVPN connection will use a specially installed network adapter (a TUN&#x2F;TAP adapter) to force all your network traffic through the slot&#x27;s OpenVPN server. This means every program on your Computer will go through the Feral slot and the server will be the point of origin for your traffic to the rest of the world.<br>
<br>
This can cause some issues with geographically aware services like banking, Paypal and email and there is no easy way to deal with this short of closing the VPN connection<br>
<br>
While it is possible to have <a href="http://openvpn.net/index.php/open-source/faq/79-client/283-can-i-run-multiple-openvpn-tunnels-on-a-single-machine.html">multiple OpenVPN tunnels on a single machine</a> it is not part of the default Feral set-up and therefore not part of this FAQ. In the default scenario you would usually only establish a single tunnel at anyone time on a device. So you would switch between VPN&#x27;s from different providers rather than use them simultaneously.<br>
<br>
Here is a picture showing the basic concept of using OpenVPN with your slot.<br>
<br>
<img src="https://raw.github.com/feralhosting/feralfilehosting/master/Feral Wiki/General/Your Feral slot is active - Part 2 - Using your slot/07 openvpn.png"><br>
<br>
<strong>Related tutorial:</strong>&nbsp; <a href="https://www.feralhosting.com/faq/view?question=5">OpenVPN - How to connect to your vpn</a><br>
<br>
<strong>Related tutorial:</strong>&nbsp; <a href="https://www.feralhosting.com/faq/view?question=220">OpenVPN - Connect on Android 4.0 and up - using OpenVPN Connect</a><br>
<br>
<h2>FTP &#x2F; SFTP &#x2F; SSH Access</h2><br>
Once you have downloaded some stuff, you have a few options on how to manage that data.<br>
<br>
<strong>FTP&#x2F;SFTP</strong> using applications like Filezilla, Bitkinex, Winscp, Cyberduck, LFTP and many more.<br>
<br>
<strong>WWW via HTTP or HTTPS</strong> via an Apache Web server where you can access your files and other Web apps, like the Web Gui for Rutorrent or Deluge.<br>
<br>
Here you will find the username, password and host you need to FTP, SFTP or SSH into your slot.<br>
		<br>
<h2>FTP</h2><br>
FTP stands for <strong>File Transfer Protocol</strong> and can be used to transfer files from your slot to your home computer or elsewhere. Most, if not all clients are capable of using FTP.<br>
<br>
FTP port is 21<br>
<br>
<a href="https://www.feralhosting.com/faq/view?question=187">FTP and SFTP basics - Filezilla</a><br>
			<br>
<h2>SFTP - Recommended</h2><br>
SFTP stands for <strong>Secure File Transfer Protocol</strong> and is similar to FTP, with the addition of encryption. SFTP is the Recommended way to securely transfer data between the server and your home computer. <br>
<br>
We recommend using the these applications on Windows.<br>
<br>
<a href="http://winscp.net/eng/download.php">WinSCP client</a>, <br>
<a href="http://www.bitkinex.com/ftp/client/bitkinex323.exe">Bitkinex</a><br>
<a href="http://filezilla-project.org/download.php">Filezilla</a><br>
<br>
For Mac, we recommend:<br>
<br>
<a href="http://cyberduck.ch/">Cyberduck</a><br>
<a href="http://filezilla-project.org/download.php">Filezilla</a><br>
<br>
Other, better solutions like <a href="http://nolobe.com/interarchy/">Interarchy</a> are not free so not recommended.<br>
<br>
<strong>Related tutorial:</strong>&nbsp; <a href="https://www.feralhosting.com/faq/view?question=187">FTP and SFTP basics - Filezilla</a><br>
<strong>Related tutorial:</strong>&nbsp; <a href="https://www.feralhosting.com/faq/view?question=27">WinSCP - usage - performing common tasks - creating torrents - unrar - symlinks and more</a><br>
<strong>Related tutorial:</strong>&nbsp; <a href="https://www.feralhosting.com/faq/view?question=28">What to do if FTP speeds are slow</a><br>
<strong>Related tutorial:</strong>&nbsp; <a href="https://www.feralhosting.com/faq/view?question=182">What is multisegmented downloading - how does it help</a><br>
<br>
<h2>FTPS&#x2F;SFTP and jailed&#x2F;limited users.</h2><br>
If you would like to share access to your slot but not share the credentials Feral provided. (see <a href="https://www.feralhosting.com/faq/view?question=14">Using your account - common questions</a> this FAQ for more info on sharing your account) you will have to manually install and configure this software according to this FAQ:<br>
<br>
<a href="https://www.feralhosting.com/faq/view?question=193">Installing an FTP daemon for extra accounts</a><br>
<br>
<h2>WWW&#x2F;HTTP Access</h2><br>
To full take advantage of your WWW you will need to follow some of the Staff and user created guides in the FAQs.<br>
<br>
All slots have access to:<br>
<br>
<a href="http://dev.mysql.com/downloads/mysql/">Mysql 5.6.12</a> - requires installation from the Install software page.<br>
<a href="http://packages.debian.org/wheezy/apache2">Apache 2.2.22-13</a><br>
<a href="http://packages.debian.org/wheezy/php5">php5 5.4.4-14</a><br>
<br>
With these you can easily make use of the WWW folder for various purpose, for example:<br>
<br>
<a href="https://www.feralhosting.com/faq/view?question=20">Putting your WWW folder to use</a><br>
<a href="https://www.feralhosting.com/faq/view?question=22">Password protect your WWW folder</a><br>
<a href="https://www.feralhosting.com/faq/view?question=52">Host a virtual host on your Feral slot</a><br>
<a href="https://www.feralhosting.com/faq/view?question=222">Ajaxplorer 5 - Basic setup</a><br>
<a href="https://www.feralhosting.com/faq/view?question=211">Wordpress - Basic setup</a><br>
<a href="https://www.feralhosting.com/faq/view?question=9">Using Mysql</a><br>
				<br>
And that is it for this FAQ. It has covered the basics and you should be well on your way to downloading some Linux Distributions!<br>
<br>
Don&#x27;t forget to Search&nbsp; the FAQs for answers to problems and things to do. The search is not that great so use <code>CTRL</code> and <code>F</code> in a browser and search to the words that match your query.<br>
<br>
