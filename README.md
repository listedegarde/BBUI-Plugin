BBUI-Plugin
===========

Plugin to make the context menu work with BBui.js

Made to be the WebWorks 2.0 version of this plugin: https://github.com/blackberry/bbUI.js/tree/master/pkg/bb10.  To make the context menu work with BBui.js and WebWorks 2.0:

1. Add copy the com.blackberry.bbui directory to your /BB10 WebWorks SDK 2.0.0.54/plugin directory
2. Add the plugin to your WebWorks 2.0 project using "webworks plugin add com.blackberry.bbui".

Known issue : this causes the app to have a black screen for approximately 1 minute before finally loading.  Inspecting from the Chrome Console reveals the following error: "NETWORK_ERR: XMLHttpRequest Exception 101: A network error occurred in synchronous requests." on line 823 of cordova.js.  The WebWorks 1.0 plugin did use "window.webworks.execAsync" instead of "window.webworks.execSync" like most other plugins, so I'm guessing that this could be at fault, but I'm not sure.

The other peculiarity of the WebWorks 1.0 version was the '"global": true,' in the manifest.json file.  Most of the other plugins had global set to false, so this is another possible place that I went wrong.

I would appreceate any feedback since this is the first WebWorks 2.0 / Cordova plugin I have ever made, and don't fully understand what's going on.  ;)

