# VLAN and Trunk Troubleshooting Guide

## Overview

This guide provides a structured approach to troubleshooting VLAN and trunk connectivity issues in enterprise networks.

## Common Symptoms

- Hosts unable to communicate across switches
- Missing VLANs
- Intermittent connectivity
- STP topology changes

## Verification Commands

### Cisco

show vlan brief
show interfaces trunk
show interfaces switchport
show spanning-tree vlan

## Troubleshooting Steps

### VLAN Validation

- Verify VLAN exists on all switches
- Confirm correct VLAN assignment
- Check VLAN status is active

### Trunk Validation

- Verify trunk mode
- Confirm allowed VLAN list
- Check native VLAN consistency

### STP Validation

- Verify root bridge placement
- Check blocked ports
- Review topology change counters

## Common Root Causes

- VLAN not created
- VLAN not allowed on trunk
- Native VLAN mismatch
- Incorrect access VLAN
- STP blocking unexpected path

## Best Practices

- Standardize VLAN numbering
- Document trunk links
- Restrict allowed VLANs
- Monitor STP events
- Validate configurations after changes
