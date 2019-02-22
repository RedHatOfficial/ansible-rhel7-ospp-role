# United States Government Configuration Baseline

[![Build Status](https://travis-ci.org/RedHatOfficial/ansible-rhel7-ospp-role.svg?branch=master)](https://travis-ci.org/RedHatOfficial/ansible-rhel7-ospp-role)
[![Ansible Role](https://img.shields.io/ansible/role/29973.svg)](https://galaxy.ansible.com/RedHatOfficial/rhel7-ospp-role)
[![GitHub release](https://img.shields.io/github/release/RedHatOfficial/ansible-rhel7-ospp-role.svg)](https://github.com/RedHatOfficial/ansible-rhel7-ospp-role/releases/latest)

Ansible remediation role for profile ospp  
Profile Title:  United States Government Configuration Baseline  
Profile Description:  
This compliance profile reflects the core set of security   
  related configuration settings for deployment of Red Hat Enterprise   
  Linux 7.x into U.S. Defense, Intelligence, and Civilian agencies.   
  Development partners and sponsors include the U.S. National Institute   
  of Standards and Technology (NIST), U.S. Department of Defense,   
  the National Security Agency, and Red Hat.    
    
  This baseline implements configuration requirements from the following   
  sources:   
    
  - Committee on National Security Systems Instruction No. 1253 (CNSSI 1253)   
  - NIST Controlled Unclassified Information (NIST 800-171)   
  - NIST 800-53 control selections for MODERATE impact systems (NIST 800-53)   
  - U.S. Government Configuration Baseline (USGCB)   
  - NIAP Protection Profile for General Purpose Operating Systems v4.0 (OSPP v4.0)   
  - DISA Operating System Security Requirements Guide (OS SRG)   
    
  For any differing configuration requirements, e.g. password lengths, the stricter   
  security setting was chosen. Security Requirement Traceability Guides (RTMs) and   
  sample System Security Configuration Guides are provided via the   
  scap-security-guide-docs package.   
    
  This profile reflects U.S. Government consensus content and is developed through   
  the OpenSCAP/SCAP Security Guide initiative, championed by the National   
  Security Agency. Except for differences in formatting to accommodate   
  publishing processes, this profile mirrors OpenSCAP/SCAP Security Guide   
  content as minor divergences, such as bugfixes, work through the   
  consensus and release processes.  
  
Benchmark ID:  RHEL-7  
 
XCCDF Version:  1.1  
  
This file was generated by OpenSCAP 1.2.17 using:  
	$ oscap xccdf generate fix --profile ospp --template urn:xccdf:fix:script:ansible xccdf-file.xml   
  
This script is generated from an OpenSCAP profile without preliminary evaluation.  
It attempts to fix every selected rule, even if the system is already compliant.  
  
How to apply this remediation role:  
$ ansible-playbook -i "192.168.1.155," playbook.yml  
$ ansible-playbook -i inventory.ini playbook.yml

## Requirements

- Ansible version 2.5 or higher

## Role Variables

To customize the role to your liking, check out the [list of variables](vars/main.yml).

## Dependencies

N/A

## Example Playbook

Run `ansible-galaxy install RedHatOfficial.rhel7-role-ospp` to
download and install the role. Then you can use the following playbook snippet.


    - hosts: all
      roles:
         - { role: RedHatOfficial.rhel7-role-ospp }


Then first check the playbook using (on the localhost):

    ansible-playbook -i "localhost," -c local --check playbook.yml

To deploy it, use (this may change configuration of your local machine!):

    ansible-playbook -i "localhost," -c local playbook.yml


## License

BSD-3-Clause

## Author Information

This Ansible remediation role has been generated from the body of security
policies developed by the ComplianceAsCode project. Please see
[https://github.com/complianceascode/content/blob/master/Contributors.md](https://github.com/complianceascode/content/blob/master/Contributors.md)
for an updated list of authors and contributors.
