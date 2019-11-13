# Remove all packages from specific repository

## To see what repos you have installed packages from

```
rpm -qa --qf "%{VENDOR} \n" | sort | uniq
```
The result should be a list of VENDOR tags. (Example form a SLES)
```
Elastic
(none)
openSUSE Build Service
SEP AG, Weyarn, Germany
SUSE LLC <https://www.suse.com/>
```

### To see the packages from a particular Vendor.

Example EPEL
```
rpm -qa --qf "%{NAME} %{VENDOR} \n" | grep "Fedora Project" | cut -d ' ' -f 1 | sort
```

Example for opensuse build service
```
rpm -qa --qf "%{NAME} %{VENDOR} \n" | grep "openSUSE Build Service"
```

## remove the packet

you could remove a singel packet.

Other way create a list and remove all with yum or zypper

```
for I in $(rpm -qa --qf "%{NAME} %{VENDOR} \n" | grep "openSUSE Build Service" | awk '{ print $1 }'); do echo -n "$I "; done
```

