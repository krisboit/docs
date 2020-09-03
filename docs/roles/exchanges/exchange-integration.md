---
id: exchange-integration
title: Exchange Integration
sidebar_label: Exchange Integration
---

# Exchange Integration

## Transaction Construction
  - NEAR requires transactions to be serialized in [Borsh](https://borsh.io/) which currently supports:
    - Rust
    - JavaScript
    - TypeScript
  <!-- Is documentation for transaction construction / ways to implement Borsh in non-supported language needed?-->

## Transaction Processing
 - [Runtime Specifications](https://nomicon.io/RuntimeSpec/README.html)
 - [Processing transactions](https://docs.near.org/docs/concepts/transaction#transaction-processing)
 - [NEAR platform errors](https://docs.near.org/docs/roles/integrator/errors/introduction#near-platform-errors)
 <!-- Should the last two links be removed as only the top link is necessary? -->

## Balance Changes
  -  Balance changes on accounts can be tracked by using our [changes endpoint](https://docs.near.org/docs/api/rpc-experimental#changes).
    **Note** Gas price can change between blocks and even for transactions with deterministic. The gas cost the cost in NEAR can also be different.

## Account Creation
  - We will soon support implicit account creation which allows exchanges to create accounts without paying for transactions. 
  - Follow the status of this feature [here](https://github.com/nearprotocol/NEPs/pull/71).

## Finality
 - RPC queries allow you to specify three types of desired finality; `optimistic`, `near-final`, and `final`.
 - Exchanges should only use [`final` finality](https://docs.near.org/docs/api/rpc-params#using-final-finality).
 - See [Blockchain Finality](https://docs.near.org/docs/roles/integrator/integrating#finality) for more information.
 <!-- Not sure if the last doc is relevant, as Bowen mentioned. -->

## Running an Archival Node
 <!--Documentation needed for running archival nodes -->

## (Optional) Staking and Delegation
 <!-- Documentation needed... Some info can be found at https://github.com/nearprotocol/stakewars and https://github.com/near/core-contracts  -->