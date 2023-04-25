# Simple and efficient smart contract for Vesting ERC20 tokens

Allows anyone to create vesting schedules for the ERC20 token the contract is initialized with. This is built both for user and other contracts to vest.

After you approve the contract for the amount of tokens you want to lock, simply call the `createVesting` function, specifying:

1. The address of the recipient of the tokens
2. The start time of the vesting schedule(if you first want a cliff and then a linear vesting, set the start time to the cliff time)
3. The duration of the vesting schedule(in days/weeks/months)
4. The unit of the duration(days/weeks/months)
5. The amount of tokens to be vested

To claim the vested tokens, a user has to only call the `release` function, specifying the address to release for. The contract will automatically go through all the schedules of the specified address, calculate the amount of tokens to be claimed and transfer them to the user.

Enjoy!
