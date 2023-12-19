## vlPOINTS

vlPOINTS is locking similar to the ve-style program of Curve. 

### Max lock

POINTS can be locked up to 1 years into vlPOINTS, which is non-transferable. They are at least locked for a week.

### vlPOINTS balance

The duration of the lock gives the amount of vlPOINTS relative to the amount locked, locking for one year gives you a vlPOINTS balance equal to the amount of POINTS locked. Locking for 6 months gives you a vlPOINTS balance of 50% of the POINTS locked.

The balance decay overtime and can be pushed back to max value by increasing the lock back to the max lock duration.


### vlPOINTS early exit
It’s possible to exit the lock early, in exchange for paying a penalty that gets distributed to the account that have vlPOINTS locked. The penalty for exiting early is the following: 
```
    min(75%, lock_duration_left / 1 year * 100%)
```
So at most you are paying a 75% penalty that starts decreasing when your lock duration goes beyond 3 months.

## vlPOINTS governance rights

* vote for the 15 candidates on the multisig
* set the treasury address in the vlPOINTS contract where the penalty is collected
* Quorum is 20%
* Voting is on snapshot for now, but at some point should be fully on-chain

## members

* members need at least 1000 vlPOINTS to get access to the member area


## Voting for the multisig

* candidates have to be members
* candidates for the multisig have to send 1000 POINTS to the treasury
* The 15 candidates with the most votes are eligible
* Out of the 15 candidates 5 are randomly drawn for the multisig

 ## Replacment on multisig

 * If one member wants to leave the multisig a replacement vote is held
 * 3 candidates with the most votes are eligible
 * 1 candidate is randomly drawn


## vlPOINTS Treasury

Panalty from exit is collected in the treasury multisig. The 3/5 multisig is public voted at least yearly or if the majority of vlPOINTS holder ask for.

## Setup

Install ape framework. See [ape quickstart guide](https://docs.apeworx.io/ape/stable/userguides/quickstart.html)

Install dependencies
```bash
npm install
```

Install [Foundry](https://github.com/foundry-rs/foundry) for running tests
```bash
curl -L https://foundry.paradigm.xyz | bash
```

```bash
foundryup
```

## Compile

Install ape plugins
```bash
ape plugins install .
```

```bash
ape compile
```

## Test

```bash
ape test
```
