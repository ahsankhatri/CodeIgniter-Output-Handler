CodeIgniter-Output-Handler
==========================

Simple hook oriented class to handle/modify output. Specially made for services in JSON to handle null values

Usage:
1) Enable $config['enable_hooks'] in config/config.php, set this to TRUE
$config['enable_hooks'] = TRUE;

2) Add this code in config/hooks.php
$hook['display_override'] = array(
    'class'    => 'OutputHandler',
    'function' => '__construct',
    'filename' => 'null_handler.php',
    'filepath' => 'hooks',
);

3) place null_handler.php in hooks folder.

And configure or add your custom function to work with it.
