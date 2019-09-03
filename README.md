# Enigma - Secret Benchmarking

## Implementation Details

- [x] Data Provider (user A) submits a dataset with [task ID, hours, rate] via an UI. [Note: this can be filler data, but should resemble something like: 4353 (ID), 32 (total hours), 123 (hourly rate)] Data Providers should be able to enter a "task name" to title the data set.

- [x] Dataset submitted by Data Provider is encrypted via Enigma-JS and submitted to the secret contract (which functions as the data storage in this example-- dataset should not be overly large).

- [x] Data Users (user B) select the "task name" from a list in a UI (for example, Generic Security Audit).

- [x] Data Users are prompted to submit quote data via the UI.

- [x] Data user data is encrypted via Enigma-JS and submitted to the secret contract.

- [x] The secret contract should compare the Data user B submitted with User A's dataset, and determine what percentile User B data is within.

- [x] The percentile result should be encrypted for User B, and returned.

- [x] User B should be able to receive and decrypt the result in their UI.

- [x] Migration scripts (if required)

- [x] Integration tests

- [x] Readme

## Issues
- `secret_contracts/src/lib.rs` -> `fn calc_percentile`, check if it is done correctly
- Enigma MST Model: `client/src/models/Enigma.ts`, dynamically retrieve contract data
- bundle size (Enigma.js & Web3 take alot of space)

## Pitfalls
- After doing `discovery start` make sure you reset [metamask](https://ethereum.stackexchange.com/questions/44311/reset-metamask-nonce)