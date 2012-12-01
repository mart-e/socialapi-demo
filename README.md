socialapi-demo
==============

This is a clone of the repository https://github.com/mixedpuppy/socialapi-demo/ to use it on a local install

Installation
------------
1. Create a new profile.  You don't want to be messing with all these prefs in a profile that you use regularly.

2. Set the following boolean prefs via about:config

        social.enabled: true
        social.active: true
        media.navigator.enabled: true
        media.navigator.permission.disabled: true
        media.peerconnection.enabled: true
        dom.disable_open_during_load: false

3. You will need NodeJS to run the provider.

    $ npm install
    $ node server.js

4. Set the SocialAPI provider, also via about:config. It's ok that the provider is named "facebook", the SocialAPI grabs the first pref prefixed with social.manifest. Note that the pref is actually a JSON string.

        social.manifest.facebook: {
          "location":"http://localhost:8888/manifest.json",
          "name":"Social Demo",
          "iconURL":"http://localhost:8888/icon.png",
          "workerURL":"http://localhost:8888/worker.js",
          "sidebarURL":"http://localhost:8888/sidebar.htm",
          "origin":"http://localhost:8888",
          "enabled":true,
          "last_modified":135101330568
        }

5. Restart the browser.

6. Have fun and tweak everything

