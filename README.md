Ejabberd >= 17.01 module to send offline user's message via POST request to target URL.
This module can call an api to send e.g. a push message. 
The request body is in application/x-www-form-urlencoded format. See the example below.


Installation
------------

When ejabberd install with .deb or .rpm installer 

-    cd /opt/ejabberd/.ejabberd-modules/sources/
-    git clone https://github.com/chiraggoti2016/mod_offline_http_post_ext.git;
-    sudo /opt/ejabberd-{your ejabbed version}/bin/ejabberdctl module_install mod_offline_http_post_ext
-	 /etc/init.d/ejabberd restart;

When ejabberd install with source - tar.gz

-    cd $HOME/.ejabberd-modules/sources/
-    git clone https://github.com/chiraggoti2016/mod_offline_http_post_ext.git;
-	 sudo ejabberdctl module_install mod_offline_http_post_ext
-	 sudo ejabberdctl stop
-	 sudo ejabberdctl start

Great, The module is now installed.

Configuration
-------------

Before install mod_offline_http_post_ext module, fill up file `/opt/ejabberd/.ejabberd-modules/sources/mod_offline_http_post_ext.yml`:
-	auth_token
-	post_url

Or Add the following to ejabberd configuration under `modules:`

```
mod_offline_http_post_ext:
    auth_token: "secret"
    post_url: "http://example.com/send_push"
```

-    auth_token - custom static token for authorize request.
-    post_url - your server's endpoint url

