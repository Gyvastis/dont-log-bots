Don't Allow Bots
=============

A fork of [Don't Log Bots](https://github.com/YOURLS/dont-log-bots).

Plugin for [YOURLS](http://yourls.org) `1.6+`. 

Description
-----------
Block bots from following a redirect through your shortened link.

Installation
------------
1. In `/user/plugins`, create a new folder named `dont-allow-bots`.
2. Drop repository files in that directory.
3. Go to the Plugins administration page ( *eg* `http://sho.rt/admin/plugins.php` ) and activate the plugin.
4. Have fun!

License
-------
'YOURLS' license, aka *"Do whatever the hell you want with it"*.
_YOURLS - MIT License_

More
----

The list of bot user agent strings has been compiled from one of my own YOURLS setup: user-agents **looking like** bots with more than 100 hits. There is no reliable way to determine if a client is a bot or not.

To check user agents on your own setup, you can try this query:

```mysql
SELECT DISTINCT `user_agent` as ua, COUNT(*) as c FROM `yourls_log` GROUP BY ua ORDER BY c DESC
```
