# How to connect to the server ? #
 * Open a terminal (unix/cmd)
 * Start an ssh session by typing the following command 
    - ssh root@172.17.145.16
    - type the password provided by the server admin

# How to make changes to the npm server after login ? #
 * Go to /root/verdaccio
    - there you will find everything related to the npm server, included the configuration file (/root/verdaccio/conf/).

# Publish your first package #
 * Install npm by download nodejs.
 * Go to the directory where your package is (cd path).
 * Type ```npm init``` and you'll have to fill the following :
    * > package name : (default_name) my_package_name
    * > version : (1.0.0) my_package_version
    * > description : Description of your package named my_package_name or default_name if you have left it blank.
    * > entry point : (index.js) [the file in which can be found the explanations of how the others are related.]
    * > test command : [your test command or leave empty]
    * > git repository : [where can be found your source code, can be empty]
    * > keywords : [keywords, can be empty]
    * > author : Your_Name [If you're the author of the package]
    * > licence : (ISC) [can be left empty in which case ISC will be the default licence]
    * > is this OK? (yes) [by default, yes]
 * Then type ```npm login  --registry http://172.17.145.16:4873```
    * enter your username if you have one. If you don't have an account on the server, ask for the admin credentials or ask to create your own account
    * your password or admin password if your using the admin account
    * your email address
 * Don't type the ip host like this 
    ~~172.17.145.16:4873~~ 
    without the http(s) before, it won't work
 * And finally, while you're still in your package repository, type :
     ```npm publish --registry http://172.17.145:4873```.
 __and YAYYY, your package is up. You can check it out by typing in a browser the ip address of the npm server.__
 
