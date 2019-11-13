# Install yum-cron for RHEL/CentOS

Test with centos 7

## Install yum-cron
install package yum-cron

## config cron hourly - update_cmd = minimal-security
change the configfile /etc/yum/yum-cron-hourly.conf to minimal-security (backup file before)

## config cron daily - update_cmd = security
change the configfile /etc/yum/yum-cron.conf to security (backup file before)

## start service yum-cron
running the service (still enable by the install part)

## check install today on /var/log/yum.log
grep the logfiles of install package today

