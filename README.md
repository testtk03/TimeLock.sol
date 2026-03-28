# TimeLock.sol
Base - Smart Contract Deployed by Remix TimeLock.sol
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract TimeLock {
    uint public unlockTime;

    constructor(uint _time) {
        unlockTime = block.timestamp + _time;
    }

    function isUnlocked() public view returns (bool) {
        return block.timestamp >= unlockTime;
    }
}
