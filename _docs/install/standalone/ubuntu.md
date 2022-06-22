---
title: "Install: Ubuntu/Debian"
nav_text: Ubuntu
category: standalone
order: 3
---

This page shows you how to install Terraspace on Ubuntu and Debian based linux systems that use the apt package manager.

## Ubuntu/Debian: apt-get install

Configure repo

    sudo su
    echo "deb https://apt.boltops.com stable main" > /etc/apt/sources.list.d/boltops.list
    curl -s https://apt.boltops.com/boltops-key.public | apt-key add -

Install

    apt-get update
    apt-get install -y terraspace

{% include install/upgrade-command.md %}

Remove

    apt-get remove -y terraspace

{% include install/wrappers.md %}

{% include install/upgrade-why.md %}

## Deb Install

You can also download the deb package and install it directly. Here are the commands:

Install

    wget https://apt.boltops.com/packages/terraspace/terraspace-latest.deb
    dpkg -i terraspace-latest.deb

You can check [terraspace-latest.deb.metadata.json](https://apt.boltops.com/packages/terraspace/terraspace-latest.deb.metadata.json) to verify the package checksum. Here's the checksum command.

    sha256sum terraspace-latest.deb

Uninstall

    dpkg -r terraspace-latest.deb
