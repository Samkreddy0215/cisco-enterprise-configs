# OSPF Troubleshooting Checklist

## Objective

Provide a structured approach to diagnosing and resolving OSPF neighbor and routing issues.

## Neighbor Verification

- show ip ospf neighbor
- Verify neighbor state is FULL
- Check Router IDs
- Verify Area IDs match

## Interface Validation

- show ip ospf interface
- Verify OSPF enabled on correct interfaces
- Check network type
- Validate hello and dead timers

## Common Issues

### Neighbor Stuck in INIT
- One-way communication
- ACL blocking OSPF packets
- Multicast issues

### Neighbor Stuck in EXSTART/EXCHANGE
- MTU mismatch
- Duplicate Router ID

### Missing Routes

- Incorrect network statements
- Area mismatch
- Route filtering
- Summarization issues

## Verification Commands

show ip ospf neighbor
show ip ospf database
show ip route ospf
show ip protocols

## Best Practices

- Use loopbacks for Router IDs
- Maintain consistent timer settings
- Document area design
- Monitor adjacency changes
- Validate route propagation after changes
