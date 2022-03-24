# Plugin Whitelist
Easy whitelist a server with ip adres and port to use your plugin! This is based on AdvancedLicense but created for fun!

![](https://img.shields.io/github/stars/Tiebienotjuh/PluginVerify)
![](https://img.shields.io/github/forks/Tiebienotjuh/PluginVerify)
![](https://img.shields.io/github/release/Tiebienotjuh/PluginVerify)
![](https://img.shields.io/github/issues/Tiebienotjuh/PluginVerify)
### Functions

- Easy to add and remove servers
- Change easy the hole website!
- Almost no use of the server.
- Customize everything!

### How to install?
1. Upload the repository to a server where NodeJS is installed.
1. You just install the needed package by run the next command `npm install`.
1. You change the port, mode, sessionsecret, username and password in config.json!
1. You start the webserver with `node index.js`.
1. Login to your url `http://ip:port/login` with the login information that you have defined in the config.json
1. Next build in the request system in your Java Minecraft plugin! You can find the code below! (Don't forget to change the url to url of your webserver!)
1. Build your plugin and test it! 
7. Give my github repository a star! Thx ;-)

### Modes

You can choose between `blacklist` and `whitelist`. But what is it?
- Als je de modus whitelist gebruikt moet elke server toegewezen worden aan de plugin!
- Als je de modus blacklist gebruikt kan elke server de plugin gebruiken maar kan je servers toevoegen die de plugin niet kunnen gebruiken!

### Java Example
If you know a better way to do this. Please contact me on discord! `Tiebienotjuh#3173`

```
URL url = new URL("http://yourwebserverip:yourwebserverport/verify?port=" + getServer().getPort());
HttpURLConnection con = (HttpURLConnection) url.openConnection();
int responseCode = con.getResponseCode();
if(responseCode == 200) {
    Bukkit.getLogger().info("Verify Server: Plugin is allowed to use!");
} else if(responseCode == 403) {
    Bukkit.getLogger().warning("Verify server: Plugin isn't allowed to use! Disabling the plugin....");
    Bukkit.getPluginLoader().disablePlugin(this);
}
```

### Details about the project
I made this for my friend called 'Daan' and i made it for him!
I made this this in NodeJS and Java. The webserver is made in NodeJS and i used the packages:
`express, express-session, quick.db, connect-flash, ejs, request`

Thanks for using it! Made with love in NodeJS and Java.
Made by Tiebienotjuh
