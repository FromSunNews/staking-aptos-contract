# Stake Contract

This project implements a staking system using the Move language on the Aptos blockchain framework. The main modules include:

1.  **Comparator** (`stake::comparator`)
    
    *   Provides a framework for comparing two elements after BCS serialization.
    *   Functions:
        *   `compare<T>`: Compares two objects of type `T`.
        *   `is_equal`, `is_smaller_than`, `is_greater_than`: Checks the comparison result.
2.  **Math Module** (`stake::math`)
    
    *   Provides utility functions for mathematical operations.
    *   Includes:
        *   `sqrt`, `pow`, `min`, `max`, `mul_div`: For common operations.
        *   Handles errors such as divide by zero and overflow.
3.  **U256 Module** (`stake::u256`)
    
    *   Implements large integer (`U256`) arithmetic.
    *   Supports addition, subtraction, multiplication, division, shifting, and comparison.
    *   Extends functionality for large numbers beyond 64-bit.
4.  **Stake Module** (`stake::stake`)
    
    *   Core module for managing staking pools and user interactions.
    *   Allows the creation, management, and participation in staking pools.
    *   Functions:
        *   `create_pool`: Allows admins to create new staking pools with specific parameters.
        *   `deposit`, `withdraw`: Users can stake and withdraw tokens from pools.
        *   `add_reward`: Admins can add rewards to pools.
        *   `emergency_withdraw`: Users can withdraw all staked tokens in case of emergency.
        *   `stop_reward`: Admin can stop reward distribution.

## Installation

Ensure you have the Aptos framework set up in your Move development environment. The project uses the Aptos Move framework as a dependency:

toml

Sao chép mã

`[dependencies.AptosFramework] git = "https://github.com/aptos-labs/aptos-core.git" rev = "testnet" subdir = "aptos-move/framework/aptos-framework"`

## How to Use

1.  **Create a Pool**: The admin can create a staking pool for specific tokens with a reward system.
2.  **Staking Tokens**: Users can stake their tokens in the created pools and earn rewards over time.
3.  **Withdraw Tokens**: Users can withdraw their staked tokens along with any earned rewards.
4.  **Emergency Withdraw**: Users can withdraw all staked tokens without waiting for the pool to end in case of an emergency.

## License

This project is licensed under the Apache-2.0 License. Original work is attributed to various sources such as the [Pontem Network](https://github.com/pontem-network/U256) and [Aptos Framework](https://github.com/aptos-labs/aptos-core).
