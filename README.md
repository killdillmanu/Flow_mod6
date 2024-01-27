# NFT-flow
This Cadence application facilitates the production and management of Non-Fungible Tokens (NFTs) by implementing the standard. Users can mint new NFTs, trade ownership of existing NFTs, deposit NFTs, and withdraw NFTs with this program.


# Description
These files contain a Cadence contract that demonstrates how to use the standard NonFungibleToken library to produce and maintain non-fungible tokens (NFTs) on the Flow network. The agreement allows for the creation of NFTs with metadata such as name, favorite cuisine, and lucky number. It also enables you to borrow, transfer, withdraw, and deposit NFTs with a unique ID in addition to these functions. The CryptoPoops contract implements the NonFungibleToken standard and provides a resource called NFT for creating NFTs with personalized data. It also specifies a Collection.It also defines a Collection resource that makes it possible to manage the NFT collection for an address. The contract also includes a Minter resource for creating NFTs and minting them into a Collection.

The CollectionPub interface defines the public functions, such as deposit, getIDs, borrowNFT, borrowAuthNFT, and withdraw, that can be used to interact with the Collection resource. The creation of Minter resources for minting NFTs and empty collections, respectively, is made possible by the functions createMinter and createEmptyCollection.

The contract sends events on contract start, NFT deposit, and NFT withdrawal. Taking everything into account, this contract provides a simple NFT implementation and demonstrates the fundamental core functionality.


## Requirements
* Access to a Flow network node.
* Cadence Compiler
* Cadence REPL
* Cadence SDK

#### Deploy the contract
* Compile the contract using the Cadence Compiler.
* Deploy the contracts "NonFungibleToken.cdc.cdc" and "NFT_1.cdc" to the Flow network node.(NOTE: deploying address should be updated on all required .cdc files) 
* Create the collection with "CreateColl.cdc"
* Mint a new NFT with "DepoNFT.cdc"
* Use Scripts to display metadata of the NFT's

#### Other Usable Functions Inside The Contract

* Withdraw an NFT

Call the getIDs() function on the Collection instance to get the list of NFT IDs you own.
Call the withdraw(withdrawID) function on the Collection instance and pass in the ID of the NFT you want to withdraw.
The NFT will be transferred back to the caller.

* Transfer an NFT

Call the borrowAuthNFT(id) function on the Collection instance and pass in the ID of the NFT you want to transfer.
Create a new instance of the Collection resource using the createEmptyCollection() function.
Call the deposit(token) function on the new Collection instance and pass in the borrowed NFT.
The NFT ownership will be transferred to the new Collection instance.

#### Reading NFT metadata
The following functions can be used to read NFT metadata:

* getIDs(): Returns the list of NFT IDs you own.
* borrowNFT(id): Returns a borrowed reference to an NFT by ID.
* borrowAuthNFT(id): Returns an authenticated borrowed reference to an NFT by ID.

The NFT resource defines the following fields:

* id: The unique identifier of the NFT.
* name: The name of the NFT.
* favouriteFood: The favourite food of the NFT.
* luckyNumber: The lucky number of the the NFT

## License
This NFT program is not licensed.
