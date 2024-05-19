# Automated VMs Setup: CentOS Web Server and Ubuntu WordPress

This repository contains the Vagrant setup files to automate the creation of two virtual machines (VMs): a CentOS web server and an Ubuntu server with a WordPress installation. 

## Table of Contents

- [Requirements](#requirements)
- [Setup Instructions](#setup-instructions)
- [VM Configuration](#vm-configuration)
  - [CentOS Web Server](#centos-web-server)
  - [Ubuntu WordPress](#ubuntu-wordpress)
- [Usage](#usage)
- [Common Issues](#common-issues)
- [Contributing](#contributing)
- [License](#license)

## Requirements

- Vagrant
- VirtualBox or another supported provider

## Setup Instructions

1. Clone the repository from GitHub and navigate into the directory.

2. Initialize the VMs by running Vagrant, which will download the necessary boxes and provision the VMs as per the configuration files.

## VM Configuration

### CentOS Web Server

- **OS**: CentOS
- **Services**: Apache HTTP Server
- **Provisioning**: Shell script to install and configure Apache

Configuration details can be found in the `Vagrantfile` and the provisioning script `scripts/centos_provision.sh`.

### Ubuntu WordPress

- **OS**: Ubuntu
- **Services**: LAMP stack (Linux, Apache, MySQL, PHP), WordPress
- **Provisioning**: Shell script to install and configure Apache, MySQL, PHP, and WordPress

Configuration details can be found in the `Vagrantfile` and the provisioning script `scripts/ubuntu_provision.sh`.

## Usage

- **Access CentOS Web Server**

  Once the VM is up and running, you can access the CentOS web server by navigating to `http://localhost:8080` in your web browser.

- **Access Ubuntu WordPress**

  Similarly, you can access the WordPress site on the Ubuntu VM by navigating to `http://localhost:8081`.

## Common Issues

- **Network Conflicts**: Ensure that the ports `8080` and `8081` are not being used by other services on your host machine.
- **Permission Issues**: Run Vagrant with sufficient permissions, especially if provisioning scripts require administrative privileges.

## Contributing

Contributions are welcome! Please fork this repository and submit a pull request for any enhancements or bug fixes.


