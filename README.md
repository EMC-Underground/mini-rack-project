# Mini-rack Project

## Goals for the project
- To provide an environment to tinker with technoligies
  + RackHD
  + Cloud Foundry
  + Puppet
  + vRA


- To provide an environment to develop code w/ P3 tools
  + Jenkins
  + Github
  + Puppet (Infra-as-code)

## Physical Layout
- 5 Servers
  + 2U
  + 4 Nics
  + 1-2 Power Supply (dependant on PDU)
  + 2 CPU
  + 96+ GB RAM
- 24+ Port Managed Switch
- Switched Rack PDU

## Pre-installed/-configured Components
- 1 server with Ubuntu
- Private Networks
  + VLAN 11 - 192.168.11.0/24 - ScaleIO Data 1
  + VLAN 12 - 192.168.12.0/24 - ScaleIO Data 2
  + VLAN 13 - 192.168.13.0/24 - CloudFoundry Private Network

## Order of Install
- External Subnet
- RackHD - BareMetal
- Puppet - Baremetal
- Windows AD w/ DNS, DHCP, PXE boot redirect - Baremetal via Puppet and RackHD
- Integrate AD into Puppet
- 2 ESXi Hosts with the SDC installed
- VCSA
- Migrate AD to VM
- Migrate RackHD to VM
- Migrate Puppet to VM
- 3rd ESXi host with the SDC installed
- ScaleIO
- CloudFoundry
- Jenkins
- Deploy labapi
- Deploy hubot
- Deploy hubot packages
