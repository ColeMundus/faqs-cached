<h1>Cron</h1>

        
Cron is a handy way of executing tasks on a schedule or at certain points. This guide will edit the crontab via SSH and will focus on two issues:<br>
<br>
1) Getting custom software started when the server is rebooted; and<br>
<br>
2) Running tasks repeatedly to a schedule<br>
<br>
In SSH do the commands described in this FAQ. If you do not know how to SSH into your slot use this FAQ: <a href="https://www.feralhosting.com/faq/view?question=12">SSH Guide - The Basics</a><br>
<br>
Your FTP &#x2F; SFTP &#x2F; SSH login information can be found on the Slot Details page for the relevant slot. Use this link in your Account Manager to access the relevant slot:<br>
<br>
<img src="https://raw.github.com/feralhosting/feralfilehosting/master/Feral%20Wiki/0%20Generic/slot_detail_link.png"><br>
<br>
You login information for the relevant slot will be shown here:<br>
<br>
<img src="https://raw.github.com/feralhosting/feralfilehosting/master/Feral%20Wiki/0%20Generic/slot_detail_ssh.png"><br>
<br>
<h2>Bringing up the crontab editor</h2><br>
To bring up the crontab editor, simply copy-paste the following command:<br>
<br>
<pre><code>crontab -e</code></pre><br>
If this is your very first time you&#x27;ll be given a choice of editors. <code>Nano</code> is fine to use so unless you have other desires simply press enter.<br>
<br>
You&#x27;ll be presented with this text:<br>
<br>
<pre><code># Edit this file to introduce tasks to be run by cron.
#
# Each task to run has to be defined through a single line
# indicating with different fields when the task will be run
# and what command to run for the task
#
# To define the time you can provide concrete values for
# minute (m), hour (h), day of month (dom), month (mon),
# and day of week (dow) or use &#x27;*&#x27; in these fields (for &#x27;any&#x27;).#
# Notice that tasks will be started based on the cron&#x27;s system
# daemon&#x27;s notion of time and timezones.
#
# Output of the crontab jobs (including errors) is sent through
# email to the user the crontab file belongs to (unless redirected).
#
# For example, you can run a backup of all your user accounts
# at 5 a.m every week with:
# 0 5 * * 1 tar -zcf &#x2F;var&#x2F;backups&#x2F;home.tgz &#x2F;home&#x2F;
#
# For more information see the manual pages of crontab(5) and cron(8)
#
# m h&nbsp; dom mon dow&nbsp;  command</code></pre><br>
This provides some basic information on crontabs - you can keep it if you like, or get rid of it if you prefer. The lines are commented out so are for information purposes only and don&#x27;t affect any cron jobs added.<br>
<br>
<h2>1 - Ensuring software starts up if the server reboots</h2><br>
Sometimes a server might need to be rebooted. Though software like torrent clients, Plex and MySQL will get restarted automatically there are many common pieces of software which don&#x27;t. A cron job will prevent you needing to manually restart things.<br>
<br>
Once in the editor, add the following line to a new line of the crontab:<br>
<br>
<pre><code>@reboot $COMMAND</code></pre><br>
The special string @reboot means the command will be run at reboot. In our example, <code>$COMMAND</code> should be replaced with whichever command you wish to run.<br>
<br>
So, for instance:<br>
<br>
<pre><code>@reboot screen -dmS autodl irssi</code></pre> <br>
That will start up irssi for you and its screen can be reattached with <code>screen -r autodl</code><br>
<br>
<h2>2 - Running things on a schedule</h2><br>
A major use of cron jobs is to get things to run on a schedule. The various configurations are outside the scope of this quick quide so a couple of example (combined with the commented out text you get in the initial crontab, provided above) should be enough to get you going. Placeholders are used throughout - diskID, usernames and paths will need to be changed!<br>
<br>
This example will execute flexget every ten minutes:<br>
<br>
<pre><code>*&#x2F;10 * * * * &#x2F;media&#x2F;diskID&#x2F;username&#x2F;flexget --cron execute</code></pre><br>
The following two are equivalent and will run a script called <code>script.sh</code> at midnight:<br>
<br>
<pre><code>@daily &#x2F;media&#x2F;diskID&#x2F;username&#x2F;script.sh</code></pre> <br>
<pre><code>0 0 * * * &#x2F;media&#x2F;diskID&#x2F;username&#x2F;script.sh</code></pre> 
<br>