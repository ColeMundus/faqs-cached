<h1>Syncthing - Basic Setup</h1>

        
<h2><a href="http://syncthing.net/">Syncthing - Secure &amp; Private</a></h2><br>
<img src="https://raw.githubusercontent.com/feralhosting/feralfilehosting/master/Feral%20Wiki/Software/Syncthing%20-%20Basic%20Setup/1.png"><br>
<br>
<h2>Install syncthing:</h2><br>
 <strong>Important note:</strong> New minor versions of this program are being released often. Please check here for the current version and modify the installation code with the current URL<br>
<br>
 <a href="https://github.com/syncthing/syncthing/releases">https:&#x2F;&#x2F;github.com&#x2F;syncthing&#x2F;syncthing&#x2F;releases</a><br>
<br>
<h3>Bash Script:</h3><br>
Will install a selected version along with a proxypass for Apache or Nginx.<br>
<br>
<pre><code>wget -qO ~&#x2F;install.syncthing <a href="http://git.io/-MNlxQ">http:&#x2F;&#x2F;git.io&#x2F;-MNlxQ</a> &amp;&amp; bash ~&#x2F;install.syncthing</code></pre><br>
The URL will be in this format:<br>
<br>
<pre><code><a href="https://server.feralhosting.com/username/syncthing/">https:&#x2F;&#x2F;server.feralhosting.com&#x2F;username&#x2F;syncthing&#x2F;</a></code></pre><br>
<h3>Manual Installation.</h3><br>
<pre><code>mkdir -p ~&#x2F;bin &amp;&amp; source ~&#x2F;.{profile,bashrc}
wget -qO ~&#x2F;syncthing.tar.gz <a href="https://github.com/syncthing/syncthing/releases/download/v0.11.26/syncthing-linux-amd64-v0.11.26.tar.gz">https:&#x2F;&#x2F;github.com&#x2F;syncthing&#x2F;syncthing&#x2F;releases&#x2F;download&#x2F;v0.11.26&#x2F;syncthing-linux-amd64-v0.11.26.tar.gz</a>
tar xf ~&#x2F;syncthing.tar.gz
mv ~&#x2F;syncthing-linux-amd64-v*&#x2F;syncthing ~&#x2F;bin&#x2F;
cd &amp;&amp; rm -rf syncthing{-linux-amd64-v*,.tar.gz}</code></pre><br>
<h2>Configure syncthing:</h2><br>
Now it is ready to run so that we can create the required configuration files.<br>
<br>
Do this command in SSH to run it:<br>
<br>
<pre><code>screen -dmS syncthing ~&#x2F;bin&#x2F;syncthing</code></pre><br>
Wait until it has fully loaded and created the required files then exit the process pressing&nbsp; and holding <code>CTRL</code> then pressing <code>c</code>. It will look like this:<br>
<br>
<img src="https://raw.githubusercontent.com/feralhosting/feralfilehosting/master/Feral%20Wiki/Software/Syncthing%20-%20Basic%20Setup/2.png"><br>
<br>
1: We run the binary<br>
2: We wait until the process has fully loaded and configured itself.<br>
3: we exit the process using <code>CTRL</code> + <code>c</code><br>
<br>
<h2>Editing the <code>config.xml</code></h2><br>
Do this command in SSH:<br>
<br>
<pre><code>nano ~&#x2F;.config&#x2F;syncthing&#x2F;config.xml</code></pre><br>
Your&nbsp; generated configuration file will load and look like this. We need to make a few changes to suit our needs.<br>
<br>
<pre><code>&lt;configuration version=&quot;11&quot;&gt;
&nbsp; &nbsp; &lt;folder id=&quot;default&quot; path=&quot;&#x2F;media&#x2F;DiskID&#x2F;username&#x2F;Sync&quot; ro=&quot;false&quot; rescanIntervalS=&quot;60&quot; ignorePerms=&quot;false&quot; autoNormalize=&quot;false&quot;&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;device id=&quot;BLYW5FJ-ZCZFS7D-UIIXDIQ-OJQUWA3-LT7TFGK-3GAPZ4S-P5AYI3M-KIKPAQL&quot;&gt;&lt;&#x2F;device&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;minDiskFreePct&gt;1&lt;&#x2F;minDiskFreePct&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;versioning&gt;&lt;&#x2F;versioning&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;copiers&gt;0&lt;&#x2F;copiers&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;pullers&gt;0&lt;&#x2F;pullers&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;hashers&gt;0&lt;&#x2F;hashers&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;order&gt;random&lt;&#x2F;order&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;ignoreDelete&gt;false&lt;&#x2F;ignoreDelete&gt;
&nbsp; &nbsp; &lt;&#x2F;folder&gt;
&nbsp; &nbsp; &lt;device id=&quot;BLYW5FJ-ZCZFS7D-UIIXDIQ-OJQUWA3-LT7TFGK-3GAPZ4S-P5AYI3M-KIKPAQL&quot; name=&quot;pallas&quot; compression=&quot;metadata&quot; introducer=&quot;false&quot;&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;address&gt;dynamic&lt;&#x2F;address&gt;
&nbsp; &nbsp; &lt;&#x2F;device&gt;
&nbsp; &nbsp; &lt;gui enabled=&quot;true&quot; tls=&quot;false&quot;&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;address&gt;127.0.0.1:8384&lt;&#x2F;address&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;apikey&gt;V9tVDYebOoiUXR0wZdyeyktgeoyYTE3X&lt;&#x2F;apikey&gt;
&nbsp; &nbsp; &lt;&#x2F;gui&gt;
&nbsp; &nbsp; &lt;options&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;listenAddress&gt;0.0.0.0:22000&lt;&#x2F;listenAddress&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;globalAnnounceServer&gt;udp4:&#x2F;&#x2F;announce.syncthing.net:22026&lt;&#x2F;globalAnnounceServer&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;globalAnnounceServer&gt;udp6:&#x2F;&#x2F;announce-v6.syncthing.net:22026&lt;&#x2F;globalAnnounceServer&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;globalAnnounceEnabled&gt;true&lt;&#x2F;globalAnnounceEnabled&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;localAnnounceEnabled&gt;true&lt;&#x2F;localAnnounceEnabled&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;localAnnouncePort&gt;21025&lt;&#x2F;localAnnouncePort&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;localAnnounceMCAddr&gt;[ff32::5222]:21026&lt;&#x2F;localAnnounceMCAddr&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;maxSendKbps&gt;0&lt;&#x2F;maxSendKbps&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;maxRecvKbps&gt;0&lt;&#x2F;maxRecvKbps&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;reconnectionIntervalS&gt;60&lt;&#x2F;reconnectionIntervalS&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;startBrowser&gt;true&lt;&#x2F;startBrowser&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;upnpEnabled&gt;true&lt;&#x2F;upnpEnabled&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;upnpLeaseMinutes&gt;60&lt;&#x2F;upnpLeaseMinutes&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;upnpRenewalMinutes&gt;30&lt;&#x2F;upnpRenewalMinutes&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;upnpTimeoutSeconds&gt;10&lt;&#x2F;upnpTimeoutSeconds&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;urAccepted&gt;0&lt;&#x2F;urAccepted&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;urUniqueID&gt;&lt;&#x2F;urUniqueID&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;restartOnWakeup&gt;true&lt;&#x2F;restartOnWakeup&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;autoUpgradeIntervalH&gt;12&lt;&#x2F;autoUpgradeIntervalH&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;keepTemporariesH&gt;24&lt;&#x2F;keepTemporariesH&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;cacheIgnoredFiles&gt;true&lt;&#x2F;cacheIgnoredFiles&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;progressUpdateIntervalS&gt;5&lt;&#x2F;progressUpdateIntervalS&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;symlinksEnabled&gt;true&lt;&#x2F;symlinksEnabled&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;limitBandwidthInLan&gt;false&lt;&#x2F;limitBandwidthInLan&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;databaseBlockCacheMiB&gt;0&lt;&#x2F;databaseBlockCacheMiB&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;pingTimeoutS&gt;30&lt;&#x2F;pingTimeoutS&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;pingIdleTimeS&gt;60&lt;&#x2F;pingIdleTimeS&gt;
&nbsp; &nbsp; &nbsp; &nbsp; &lt;minHomeDiskFreePct&gt;1&lt;&#x2F;minHomeDiskFreePct&gt;
&nbsp; &nbsp; &lt;&#x2F;options&gt;
&lt;&#x2F;configuration&gt;</code></pre><br>
<strong>Change 1:</strong> The WebUi address and port to port between the range of <code>10001</code> to <code>49999</code>:<br>
<br>
<pre><code>&lt;address&gt;127.0.0.1:8384&lt;&#x2F;address&gt;</code></pre><br>
Make sure the hostname is set to <code>0.0.0.0</code> and port is changed. For example:<br>
<br>
<pre><code>&lt;address&gt;0.0.0.0:29384&lt;&#x2F;address&gt;</code></pre><br>
<strong>Change 2:</strong> The programs listening port to port between the range of <code>10001</code> to <code>49999</code> that is NOT the default <code>22000</code>:<br>
<br>
<pre><code>&lt;listenAddress&gt;0.0.0.0:22000&lt;&#x2F;listenAddress&gt;</code></pre><br>
Change it to something else, for example:<br>
<br>
<pre><code>&lt;listenAddress&gt;0.0.0.0:12532&lt;&#x2F;listenAddress&gt;</code></pre><br>
<strong>Change 3:</strong><br>
<br>
Find these settings:<br>
<br>
<pre><code>&lt;localAnnounceEnabled&gt;true&lt;&#x2F;localAnnounceEnabled&gt;
&lt;startBrowser&gt;true&lt;&#x2F;startBrowser&gt;
&lt;upnpEnabled&gt;true&lt;&#x2F;upnpEnabled&gt;</code></pre><br>
And set them to false:<br>
<br>
<pre><code>&lt;upnpEnabled&gt;false&lt;&#x2F;upnpEnabled&gt;</code></pre><br>
<br>
If you can&#x27;t find upnpEnabled, it might be called natEnabled in newer versions:<br>
<br>
<pre><code>&lt;natEnabled&gt;false&lt;&#x2F;natEnabled&gt;</code></pre><br>
<br>
Then press and hold <code>CTRL</code> and then press <code>x</code> to save. Press <code>y</code> to confirm.<br>
<br>
<h2>Accessing the Webui:</h2><br>
Now we are ready to relaunch the properly configured syncthing so that we can access and use the WebUi.<br>
<br>
In SSH execute this command:<br>
<br>
<pre><code>screen -dmS syncthing ~&#x2F;bin&#x2F;syncthing</code></pre><br>
Now the WebUi should load on the port we configured earlier.<br>
<br>
<pre><code><a href="http://server.feralhosting.com:PORT">http:&#x2F;&#x2F;server.feralhosting.com:PORT</a></code></pre><br>
<strong>Important note:</strong> You can use https if you accept the invalid cert<br>
<br>
This is what you will see when the syncthing WebUi loads, the first thin we need to do it click on the Options icon in the top right:<br>
<br>
<img src="https://raw.githubusercontent.com/feralhosting/feralfilehosting/master/Feral%20Wiki/Software/Syncthing%20-%20Basic%20Setup/3.png"><br>
<br>
Now click on <code>Settings</code>:<br>
<br>
<img src="https://raw.githubusercontent.com/feralhosting/feralfilehosting/master/Feral%20Wiki/Software/Syncthing%20-%20Basic%20Setup/4.png"><br>
<br>
Inside the settings you can set a usertname and password for the WebUi. Do this now:<br>
<br>
<img src="https://raw.githubusercontent.com/feralhosting/feralfilehosting/master/Feral%20Wiki/Software/Syncthing%20-%20Basic%20Setup/5.png"><br>
<br>
You will need to restart the syncthing server for this to take effect:<br>
<br>
<img src="https://raw.githubusercontent.com/feralhosting/feralfilehosting/master/Feral%20Wiki/Software/Syncthing%20-%20Basic%20Setup/6.png"><br>
<br>
<h2>Repository settings:</h2><br>
Each repository can be configured via the <code>Edit</code> button:<br>
<br>
<img src="https://raw.githubusercontent.com/feralhosting/feralfilehosting/master/Feral%20Wiki/Software/Syncthing%20-%20Basic%20Setup/7.png"><br>
<br>
This is the options window for a repository:<br>
<br>
<img src="https://raw.githubusercontent.com/feralhosting/feralfilehosting/master/Feral%20Wiki/Software/Syncthing%20-%20Basic%20Setup/8.png"><br>
<br>
<h2>Adding nodes:</h2><br>
<a href="https://github.com/syncthing/syncthing/releases">Syncthing Downloads</a><br>
<br>
You will need to install and configure other syncthing instances on your local or mobile devices then use the <code>Show ID</code> in the Options to see your node ID.<br>
<br>
<img src="https://raw.githubusercontent.com/feralhosting/feralfilehosting/master/Feral%20Wiki/Software/Syncthing%20-%20Basic%20Setup/9.png"><br>
<br>
<img src="https://raw.githubusercontent.com/feralhosting/feralfilehosting/master/Feral%20Wiki/Software/Syncthing%20-%20Basic%20Setup/10.png"><br>
<br>
Once you have this you can add nodes to your server instance to sync files.<br>
<br>
<h2>Help and further reading:</h2><br>
<a href="https://discourse.syncthing.net/category/documentation">https:&#x2F;&#x2F;discourse.syncthing.net&#x2F;category&#x2F;documentation</a><br>
<br>
