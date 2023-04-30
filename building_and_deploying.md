# Deploying an Ink! based Smart Contract on a Substrate Node

To deploy an ink! contract on a substrate node, you can follow these steps:

## Install the required tools:
   - Rust programming language
   - ink! CLI (`cargo install cargo-contract`)
   - Substrate node template or any substrate based blockchain: Clone this to deploy https://github.com/GlobalBoost/impactprotocol
   - Polkadot JS extension for your browser (for testing and interacting with your contract)

## Create your ink! contract 
   - Create your contract ```cargo contract new first_contract```
   - Then go inside the created contract folder ```cd first_contract```
   - You will see a ```lib.rs``` file and a ```Cargo.toml```
   - Add your contract logic in the ```lib.rs``` file 
   - Add your dependencies in the ```Cargo.toml``` file
  
## Build your contract using the command below
  
   - ```cargo +nightly contract build```
   - You will see a target folder generated with the artifacts which you will be needing in the next step
  
## Deploying your contract on the impact chain 

   - Open the Polkadot JS UI in your browser and connect it to your local node. You can do this by clicking on the "Settings" icon on the top right corner of the page and selecting your node from the dropdown menu.

   - In the "Developer" section of the UI, click on "Contracts" and then you will redirected to Contract upload page where you can see any existing contracts that is being uoloaded in the chain. To Deploy your contract click on the ```Upload & Deploy Code``` button
   
   - You will see a popup asking the metadata json file, select the json file from your contract located in the `target/ink` directory by clicking on the "Choose File" button.

   - Next it will ask for the compiled WASM contract file the "Upload WASM" page, select the compiled Wasm file from your contract located in the `target/ink/` directory by clicking on the "Choose File" button. 

   - Click on "Next" button and you can choose the contructor if you have multiple to initialize your contract

   - On the "Review WASM" page, you can view information about your contract, such as its size and hash. 

   - Click on "Deploy" to deploy your contract. You will be prompted to fill in the contract metadata, such as name, version, and author.

   - Once the contract is deployed, you can interact with it using the Polkadot JS extension. You can do this by going to the "Explorer" section of the UI and selecting your contract from the dropdown menu. 

   - From there, you can view information about your contract, such as its storage and calls. You can also test and interact with your contract by clicking on the "Contract" tab and using the provided UI to call its functions.

That's it! You've successfully deployed an ink! contract on a substrate node using the UI.
 
   
   
   
