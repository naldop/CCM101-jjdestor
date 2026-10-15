# Security Audit Report

## Chapter 8 Security Concepts

### The Principle of Least Privilege (PoLP)

The Principle of Least Privilege means that every user, application, or service should be given only the minimum access it needs to do its job, and nothing more. It matters for cloud user accounts because if an account is stolen or misused, the damage is limited to what that account was allowed to touch. A developer who only needs to read logs should not be able to delete servers or change billing settings.

### Attack Surface

An attack surface is the total number of points where an attacker could try to get into or extract data from a system. For a virtual machine, this includes open network ports, running services, installed software, user accounts, and any weak or default configurations. The more of these that are exposed, the more opportunities an attacker has, so reducing the attack surface (closing unused ports, removing unneeded services) makes the VM harder to compromise.

### Default Deny Policy

A Default Deny Policy blocks all traffic by default and only allows connections that have been explicitly approved. It is safer than trying to block specific hackers because the list of possible attackers and attack methods is endless and constantly changing, while the list of legitimate services we actually need is short and known. With default deny, anything we forgot about or did not anticipate is blocked automatically instead of being left open by mistake.
