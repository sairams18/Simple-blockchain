# Simple-blockchain

Working of the Code:
This code creates a blockchain using a combination of two classes: Block and Blockchain. Here's a step-by-step explanation of how it works:

1. Block Class:
The Block class represents a single block in the blockchain.

Each block contains:
data: The content to be stored in the block (e.g., "First Block", "Second Block").
prev_hash: The hash of the previous block in the chain, used to ensure the chain's integrity.
hash: The hash of the current block's data, calculated using the calc_hash() method.
calc_hash(): This method uses the SHA-256 algorithm (from the hashlib library) to generate a unique hash for the block based on its data. The data is first encoded to UTF-8, and then its hash is calculated and returned as a hexadecimal string.

3. Blockchain Class:
The Blockchain class represents the entire chain of blocks (the blockchain itself).

It contains:
chain: A list of blocks that starts with the "Genesis Block" (the first block of the chain).
create_genesis_block(): This method initializes the blockchain by creating the first block, called the "Genesis Block." Its prev_hash is set to "0" since it has no previous block.

add_block(): This method adds a new block to the blockchain:
It fetches the previous block (the last block in the chain list).
It creates a new Block with the provided data and the hash of the previous block as the prev_hash.
The new block is then appended to the blockchain.

3. Blockchain Construction and Printing:
A Blockchain object is created, automatically initializing it with the Genesis Block.
Three additional blocks are added with the data "First Block," "Second Block," and "Third Block."
The code then prints out each block's data, prev_hash, and hash for all blocks in the blockchain, allowing you to see how the blocks are chained together via hashes.

This code implements a simple blockchain where each block contains data, a reference to the previous block's hash, and its own hash generated using the SHA-256 algorithm. The blockchain starts with a "Genesis Block" (the first block), and additional blocks can be added with data like "First Block," "Second Block," and "Third Block."

Output Description:
The output will display the following for each block:
Data : The content stored in the block (e.g., "Genesis Block," "First Block," etc.).
Previous hash : The hash of the previous block (for the Genesis block, this will be "0").
Hash: The SHA-256 hash value of the current block's data.

The output will show these values for the genesis block and the three added blocks in sequence.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
