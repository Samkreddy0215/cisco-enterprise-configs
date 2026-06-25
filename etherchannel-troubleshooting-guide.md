# EtherChannel Troubleshooting Guide

## Overview

EtherChannel combines multiple physical links into a single logical interface to increase bandwidth and provide redundancy.

## Common Symptoms

- Port-channel not forming
- One or more member links suspended
- Traffic imbalance
- Intermittent connectivity

## Verification Commands

### Cisco

show etherchannel summary
show etherchannel port-channel
show interfaces port-channel
show lacp neighbor
show pagp neighbor

## Troubleshooting Checklist

### Physical Layer

- Verify cable connectivity
- Confirm interface status
- Check speed and duplex

### Configuration

- Ensure matching channel-group number
- Verify switchport mode
- Confirm trunk or access configuration
- Validate allowed VLANs
- Check native VLAN consistency

### Protocol

- Verify both sides use the same protocol:
  - LACP
  - PAgP
  - On (static)

### Load Balancing

- Review load-balancing method
- Confirm traffic distribution across links

## Common Root Causes

- VLAN mismatch
- Trunk configuration mismatch
- Speed or duplex mismatch
- LACP mode mismatch
- Unsupported interface configuration

## Best Practices

- Use LACP for dynamic negotiation
- Configure identical settings on all member interfaces
- Monitor port-channel health regularly
- Document member interfaces and channel IDs
- Validate failover after maintenance
