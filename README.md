---
services: app-service\web, app-service
platforms: java

---

# Java sample for Azure App Service - Coffee Shop



### Serving Java apps in App Service

This sample uses the Tomcat server provided by App Service. You can serve Java web apps in 
[a variety of ways](https://azure.microsoft.com/en-us/documentation/articles/web-sites-java-custom-upload/): 
with a web server provided by App Service, with a custom server, or with a server embedded in your 
WAR/JAR.

<a name="structure" />
### Folder structure

The main thing in the repo is a `webapps` folder with ROOT.war. The Tomcat/Jetty server in App Service
will look inside this folder for web apps to host. ROOT.war represents the default web app (at the site root). Any
WAR file that's otherwise named represents a web app accessbile at `~/<WARfilename>`. 

Also included in the repo is the Web.config file, that uses the 
[httpPlatformHandler](http://www.iis.net/downloads/microsoft/httpplatformhandler) to tell IIS to be a proxy between
HTTP requests and the Tomcat 8 server. You don't actually need this file if you enable Java for your app through the 
[portal](https://portal.azure.com) UI.

### License

See [LICENSE](LICENSE).
