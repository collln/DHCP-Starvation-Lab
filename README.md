# DHCP-yersinia-lab
This repo will hold all of the materials related to my DHCP Starvation lab using yersinia

# Introduction

This is a lab I have created to demonstrate how an attacker can use DHCP Starvation in order to cause a Denial of Service to a network.

# Architecture

As I do not have access to all of the physical hardware and software licenses required to do this with real devices (Cisco Routers and switches, multiple Linux PCs, etc.) I have done this lab completely virtually. Also, since virtualization proved to be a huge pain to do on macOS with an Apple Silicon processor, I chose to use cloud resources (Google Cloud Compute Engine) instead of my own hardware resources for the project. In summary, using a e2-standard-4 machine in Google Cloud Compute, I ran an Ubuntu VM which would act as the host for my GNS3 server. Alongside the GNS3 server, I have a Docker engine running that is creating the container for Alpine Linux machine. The reason I chose Alpine Linux over Kali Linux is I was running into issues with Kali crashing my entire cloud instance, most likely due to it being hardware intensive.Finally, alongside the server and Docker engine I am running Dynamips which is hosting my emulated Cisco3750 routers.


The full Architecture looks like this:
<img width="1360" height="1400" alt="image" src="https://github.com/user-attachments/assets/d0e5c576-cfe7-41b5-be8a-2daf99c30530" />

## How does DHCP Starvation work?


## Sources used 
https://www.cisco.com/c/en/us/td/docs/switches/lan/csbss/CBS220/CLI-Guide/b_220CLI/ip_dhcp_snooping_commands.pdf
