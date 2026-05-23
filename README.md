# School Management System (Soroban Smart Contract)

A blockchain-based School Management System built using **Rust** and the **Soroban SDK (Stellar smart contracts)**.  
The contract manages student registration, tuition payments, and payment history on-chain in a transparent and immutable way.

---

## Features

- Register students with name, wallet address, and class
- Retrieve student details by ID
- Process tuition payments using Stellar tokens
- Track total payments per student
- Maintain full payment history per student
- Emit payment events for transparency

---

## Project Structure
contracts/
└── school-management/
├── src/
│ ├── school_management.rs # Main contract logic
│ ├── storage.rs # Data structures (Student, Class, Payment)
│ ├── events.rs # Event definitions
│ └── error.rs # Custom errors
├── test.rs # Unit tests
└── Cargo.toml



---

## Core Data Models

### StudentDetails
- student_id
- name
- wallet_address
- class_name
- total_paid
- is_registered

### Class (Enum)
- Primary
- HighSchool
- College

### Payment
- student_id
- amount
- timestamp

---

## Smart Contract Functions

### Initialize Contract
Initializes admin and token address.

```rust
__constructor(env, admin, token)


## Deployed smart contract address
CCPB5POOJKUEELLR26FWP6MCDXCFACG2EF7MI76KFGHAQ2V4YZIVI2ER
