# graylog2

This installation script will perform an automated install of [Graylog2](http://graylog2.org)
on Ubuntu 12.04/12.10/13.10/14.04 and will be updated as times goes on.

> NOTE: This repo is no longer updated or maintained.
>
> Update 02/21/2014 - Graylog2 v0.12.0 no longer maintained - v0.20.x is the
> going forward version (The script to use now is for version v0.20.x)
>
> Update 04/30/2014 - All older unmaintained v.0.12.0 scripts are in `graylog2/Old_Scripts`
>
> Update 01/21/2015 - Newest versions maintained are 0.9x.x
>
> Update 11/19/2015 - A note about this repo and scripts....No further development
> is being done. For a newer version (Not always up to date) using Ansible for
> deployments can be found at <https://github.com/mrlesmithjr/ansible-graylog>

## Installation steps

### Ubuntu

```bash
sudo apt-get -y install git
cd ~
git clone https://github.com/mrlesmithjr/graylog2
chmod +x ./graylog2/install_graylog2_90_ubuntu.sh
```

To change your ip address of the server you are installing on you will need to edit the script or let the script auto detect your IP for you. The default is auto detect. If you use the default of auto detect skip editing the file and continue on.

Edit the file

```bash
nano ./graylog2/install_graylog2_90_ubuntu.sh
```

Save the file with ctrl^x.

Now enter the following to start running the script.

```bash
cd ~
sudo ./graylog2/install_graylog2_90_ubuntu.sh
```

### Debian 6.0

Within the github repository there is also a script to automate a Debian 6.0 Graylog2 (v0.12.0) installation. If you are installing on Debian 6.0 run the following instead.

```bash
chmod +x ./graylog2/Old_Scripts/install_graylog2_debian.sh
cd ~
./graylog2/Old_Scripts/install_graylog2_debian.sh
```

### CentOS

There is also a CentOS script for installing Graylog2. Thanks to boardstretcher for the help on this. <https://github.com/boardstretcher>

```bash
chmod +x ./graylog2/install_graylog2_20_centos.sh
./graylog2/install_graylog2_20_centos.sh
```

## Uninstall steps for Preview/RC/Final v0.20.0 releases

```bash
cd ~
mv graylog2 graylog2.old
git clone <https://github.com/mrlesmithjr/graylog2/>
chmod +x ./graylog2/Uninstall_Scripts/uninstall_graylog2_preview_ubuntu.sh
sudo ./graylog2/Uninstall_Scripts/uninstall_graylog2_preview_ubuntu.sh
```

## Upgrade steps from Preview/RC to Final v0.20.0 releases (**_Use with caution as of now_**) \*\*Not for v0.12.0 to v0.20.x versions!!!

```bash
cd ~
mv graylog2 graylog2.old
git clone <https://github.com/mrlesmithjr/graylog2/>
chmod +x ./graylog2/Upgrade_Scripts/upgrade_to_graylog2_20_ubuntu.sh
sudo ./graylog2/Upgrade_Scripts/upgrade_to_graylog2_20_ubuntu.sh
```

## Author Info

-   [@mrlesmithjr](https://www.twitter.com/mrlesmithjr)
-   [EverythingShouldBeVirtual](http://everythingshouldbevirtual.com)
