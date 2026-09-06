# Operations and Rollout

## Safe rollout
1. Run with `--check --diff` against a representative non-production host.
2. Review service restart impact.
3. Apply to a small canary group.
4. Validate SSH access, audit service health, and application connectivity.
5. Expand in controlled batches.

## Rollback
Keep the previous rendered SSH configuration and baseline version available. Any control that could affect remote access should be canaried before broad rollout.

## Exception handling
Exceptions should be explicit variables or inventory overrides with documented owners and expiry dates rather than manual changes on hosts.
