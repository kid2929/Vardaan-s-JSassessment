# NFT Minting Project

A simple JavaScript project for minting NFTs with metadata and displaying their details.

## Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
- [Functions](#functions)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Overview

This project allows users to mint NFTs by creating objects with specific metadata and storing them in an array. It includes functions to mint new NFTs, list all minted NFTs, and get the total supply of NFTs.

## Installation

No special installation is required for this project. You just need a modern web browser or Node.js environment to run the script.

## Usage

To use the project, copy the code into a JavaScript file and run it using a web browser console or Node.js. The script includes sample function calls to mint NFTs and display their details.

### Steps

1. Copy the provided code into a file named `nft.js`.
2. Open the terminal or command prompt.
3. Navigate to the directory containing `nft.js`.
4. Run the script using Node.js:

    ```bash
    node nft.js
    ```

### Example Code

```javascript
// create a variable to hold your NFT's
const NFTs = [];

// this function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function mintNFT(_name, _eyeColor, _shirtType, _bling) {
    const NFT = {
        "name": _name,
        "eyeColor": _eyeColor,
        "shirtType": _shirtType,
        "bling": _bling
    };
    NFTs.push(NFT);
    console.log("Minted: " + _name);
}

// create a "loop" that will go through an "array" of NFT's
// and print their metadata with console.log()
function listNFTs() {
    for (let i = 0; i < NFTs.length; i++) {
        console.log("\nID: \t\t" + (i + 1));
        console.log("Name: \t\t" + NFTs[i].name);
        console.log("Eye Color: \t" + NFTs[i].eyeColor);
        console.log("Shirt Type: \t" + NFTs[i].shirtType);
        console.log("Bling: \t\t" + NFTs[i].bling);
    }
}

// print the total number of NFTs we have minted to the console
function getTotalSupply() {
    console.log("\nTotal NFTs Minted: " + NFTs.length);
}

// call your functions below this line
mintNFT("Akash", "Brown", "Linen", "Gold Chain");
mintNFT("Vardaan", "Brown", "Linen", "Gold Chain");
mintNFT("Rounit", "Brown", "Linen", "Gold Chain");
mintNFT("Sasha", "Brown", "Linen", "Gold Chain");
listNFTs();
getTotalSupply();
```

## Functions

### mintNFT

Mints a new NFT with the given metadata and stores it in the `NFTs` array.

```javascript
function mintNFT(_name, _eyeColor, _shirtType, _bling)
```

- `_name` (string): The name of the NFT.
- `_eyeColor` (string): The eye color of the NFT.
- `_shirtType` (string): The type of shirt the NFT is wearing.
- `_bling` (string): The type of bling the NFT has.

### listNFTs

Lists all minted NFTs and prints their metadata to the console.

```javascript
function listNFTs()
```

### getTotalSupply

Returns the total number of NFTs minted.

```javascript
function getTotalSupply()
```

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/yourFeature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/yourFeature`).
5. Open a pull request.

## License

Distributed under the MIT License. See `LICENSE` for more information.

## Acknowledgements

- Thanks to the JavaScript and blockchain communities for inspiration and resources.
- Special thanks to anyone who contributed to this project.
