This is a Firefox OS App that uses the following external libraries  
Brick.js https://developer.mozilla.org/en-US/Apps/Developing/Web_components  
Three.js http://threejs.org/  
A modified version of the Google Globe.js WebGl Experiment - https://github.com/dataarts/webgl-globe/tree/master/globe  
and Cordova http://cordova.apache.org/  

If you want to run this you will need to have Cordova installed and a project created  

    $ cordova create sample org.mozilla.cordovaSample "Cordova Sample"

cd to the `sample` directory and delete the `www` folder
checkout the code into this directory.

    git clone https://github.com/mozilla-cordova/cordovasample www     

The Geolocation example uses Three.js and Globe.js and functions better on later versions of Firefox OS 1.2 or greater  

See Hacks Blog Post for more details  
https://hacks.mozilla.org/2014/02/building-cordova-apps-for-firefox-os/

Add Firefox OS as a platform:

    cordova platform add firefoxos

Make sure to use the cordova plugin add command to add the following plugins:  
  'org.apache.cordova.camera',  
  'org.apache.cordova.contacts',  
  'org.apache.cordova.device',  
  'org.apache.cordova.device-motion',  
  'org.apache.cordova.device-orientation',  
  'org.apache.cordova.dialogs',  
  'org.apache.cordova.file',  
  'org.apache.cordova.geolocation',  
  'org.apache.cordova.inappbrowser',  
  'org.apache.cordova.vibration'  

For battery-status you need the currently unpublished version from github:

    cordova plugin add https://github.com/apache/cordova-plugin-battery-status

Currently you will need to take the manifest.webapp file in the source and copy it to the merges/firefoxos directory
