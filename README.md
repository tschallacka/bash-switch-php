# bash: switch_php
A commandline utility to aid developers switching php versions easily which are used in console and apache2

install the switch_php file in ~/bin

run `chmod +x ~/bin/switch_php`

## usage

```bash
switch_php [version number]
```

If you run just switch_php you get an overview of which php versions are installed on your system.

> $~> switch_php  
> Please provide a version to switch to. Available versions are  
> 7.1 7.2 7.3 7.4 8.0   
> usage: switch_php [version number]  

if you run switch_php with a php version number it will try to switch to that version number

> $~> switch_php 7.3  
> Module php7.2 disabled.  
> To activate the new configuration, you need to run:  
>  systemctl restart apache2  
> Considering dependency mpm_prefork for php7.3:  
> Considering conflict mpm_event for mpm_prefork:  
> Considering conflict mpm_worker for mpm_prefork:  
> Module mpm_prefork already enabled  
> Considering conflict php5 for php7.3:  
> Enabling module php7.3.  
> To activate the new configuration, you need to run:  
>   systemctl restart apache2  
> Restarting apache  
> update-alternatives: using /usr/bin/php7.3 to provide /usr/bin/php (php) in manual mode  

## requirements

sudo priveleges. It uses sudo to set the correct permissions.
