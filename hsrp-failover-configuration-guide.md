# HSRP Failover Configuration Guide

## Overview

HSRP (Hot Standby Router Protocol) provides gateway redundancy by creating a virtual IP address shared between multiple routers.

## Components

- Active Router
- Standby Router
- Virtual IP Address
- Priority
- Preemption

## Sample Configuration

interface GigabitEthernet0/0
 ip address 10.10.10.2 255.255.255.0
 standby 10 ip 10.10.10.1
 standby 10 priority 110
 standby 10 preempt

## Verification Commands

show standby brief
show standby
show ip interface brief

## Troubleshooting

- Verify HSRP state
- Check virtual IP configuration
- Confirm interface status
- Validate priority settings
- Review failover events

## Best Practices

- Enable preemption on the primary router
- Track critical uplink interfaces
- Use consistent HSRP group numbering
- Document virtual gateway assignments
- Test failover during maintenance windows
