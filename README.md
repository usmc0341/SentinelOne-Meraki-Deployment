# SentinelOne-Meraki-Deployment
# Parent Repository Usage Guide

This repository contains scripts and resources to deploy SentinelOne agents using Meraki. 

## Table of Contents
- [Resources Preparation](#resources-preparation)
- [Installation Script](#installation-script)
- [Packaging for Meraki](#packaging-for-meraki)
- [Meraki Deployment Overview](#meraki-deployment-overview)

## Resources Preparation
Before starting the installation process, ensure that you have the following:
- SentinelOne agent `.pkg` file
- Site token or group token
- Mobileconfig files from the Jamf portion of SentinelOnes macOS installation documentation

## Installation Script
Use the provided helper script to install the SentinelOne agent on the remote endpoint. The script can be found in the `scripts` directory.

## Packaging for Meraki
Create a deployment package for use with Meraki using the `Packages` tool. Place the helper script, your site/group token file `com.sentinelone.registration-token`, and your SentinelOne agent `.pkg` file in a new directory.

## Meraki Deployment Overview
The deployment process involves the following steps:
1. Prepare SentinelOne deployment package
2. Upload mobileconfig files to Meraki SM
3. Add SentinelOne deployment package to Meraki SM applications catalog
4. Create Meraki SM target group
5. Tag target devices for profile installation
6. Verify profile installation to target devices and tag them for deployment

For detailed instructions, refer to the documentation files in the `docs` directory.

