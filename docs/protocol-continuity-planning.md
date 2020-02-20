# Protocol Continuity Planning 

Protocol Continuity Planning is the process of creating systems of prevention and recovery to deal with potential threats to a protocol. In addition to prevention, the goal is to enable ongoing operations before and during execution of disaster recovery, for example should an admin key be compromised.

## Prepare for failure

Any non-trivial contract will have errors in it. Your code must, therefore, be able to respond to bugs and vulnerabilities gracefully.

  - Pause the contract when things are going wrong ('circuit breaker')
  - Manage the amount of money at risk (rate limiting, maximum usage)
  - Have an effective upgrade path for bugfixes and improvements

## Rollout carefully

It is always better to catch bugs before a full production release.

  - Test contracts thoroughly, and add tests whenever new attack vectors are discovered
  - Provide [bug bounties](software_engineering.md#bug-bounty-programs) starting from alpha testnet releases
  - Rollout in phases, with increasing usage and testing in each phase

## Keep contracts simple

Complexity increases the likelihood of errors.

  - Ensure the contract logic is simple
  - Modularize code to keep contracts and functions small
  - Use already-written tools or code where possible (eg. don't roll your own random number generator)
  - Prefer clarity to performance whenever possible
  - Only use the blockchain for the parts of your system that require decentralization

## Stay up to date

Keep track of new security developments.

  - Check your contracts for any new bug as soon as it is discovered
  - Upgrade to the latest version of any tool or library as soon as possible
  - Adopt new security techniques that appear useful

  ---
  sources: [consensys smart contract best practices](https://github.com/ConsenSys/smart-contract-best-practices/)