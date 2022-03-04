# Plugin Whitelist
Easy whitelist a server with ip adres and port to use your plugin! This is based on AdvancedLicense but created for fun!
![](https://img.shields.io/github/stars/PluginVerify) ![](https://img.shields.io/github/forks/Tiebienotjuh/PluginVerify) ![](	https://img.shields.io/github/stars/Tiebienotjuh/PluginVerify) ![](https://img.shields.io/github/license/Tiebienotjuh/PluginVerify)
### Functions

-  Easy to add and remove servers
- Change easy the hole website!
- Almost no use of the server.
- Customize everything!

### How to install?
1. Upload the folder "web" to a server where NodeJS is installed.
1. You just install the needed package by run the next command `npm install`.
1. You change the port, sessionsecret, username and password in config.json!
1. You start the webserver with `node index.js`.
1. Next build in the request system in your Java Minecraft plugin! You can find the code below! (Don't forget to change the url to url of your webserver!)
1. Build your plugin and test it! 
7. Give my github repository a star! Thx ;-)

### Java Example
If you know a better way to do this. Please contact me on discord! `Tiebienotjuh#3173`

```
@Override
    public void onEnable() {
        URL url = new URL("http://yourwebserverip:yourwebserverport/verify?port=" + getServer().getPort());
        HttpURLConnection con = (HttpURLConnection) url.openConnection();
        int responseCode = con.getResponseCode();
        if(responseCode == 200) {
            Bukkit.getLogger().info("Verify Server: Plugin is whitelisted!");
        } else if(responseCode == 403) {
            Bukkit.getLogger().warning("Verify server: Plugin isn't whitelisted! Disabling the plugin....");
            Bukkit.getPluginLoader().disablePlugin(this);
        }
    }
```

### Details about the project
I made this for my friend called 'Daan' and i made it for him!
I made this this in NodeJS and Java. The webserver is made in NodeJS and i used the packages:
`express, express-session, quick.db, connect-flash, ejs`

Thanks for using it! Made with love in NodeJS and Java.
Made by Tiebienotjuh
