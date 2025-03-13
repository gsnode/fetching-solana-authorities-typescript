Solana Token Authorities Checker using TypeScript
====================================================

Description:
------------
This repository provides a simple project that demonstrates how to fetch token authorities on Solana using TypeScript. 
It includes functions to check the freeze authority, mint authority, and update authority for a given token mint.
This project is ideal for developers who want to quickly retrieve and verify token authority information using 
a reliable RPC endpoint from gsnode.io.

Requirements:
-------------
- Node.js (v18 LTS is recommended for stability)
- npm
- TypeScript (installed globally or locally)
- ts-node (for running TypeScript files directly)
- @solana/web3.js package
- @metaplex-foundation/js package

Installation:
-------------
1. Clone the repository (or download the code) into your project folder.
   Example (if using GitHub):
       git clone https://github.com/gsnode/fetching-solana-authorities-typescript.git
       cd fetching-solana-authorities-typescript

2. Initialize the Node.js project (if not already done):
       npm init -y

3. Install the required packages:
       npm install @solana/web3.js @metaplex-foundation/js
       npm install --save-dev typescript ts-node

4. Create a tsconfig.json file in your project root with the following content:
       
       {
         "compilerOptions": {
           "target": "ES2020",
           "module": "NodeNext",
           "moduleResolution": "nodeNext",
           "esModuleInterop": true,
           "skipLibCheck": true
         },
         "include": ["*.ts"]
       }

5. (Optional) In your package.json, add the following line to use ESM:
       
       "type": "module"

Usage:
------
1. Open the file "fetch-solana-authorities.ts" in your project folder. Replace the placeholder
   "INSERT_MINT_ADDRESS_HERE" **with a valid Solana token mint address** (a base58 string).

2. To run the TypeScript file directly, execute the following command in your terminal:
       
       node --loader ts-node/esm --experimental-specifier-resolution=node fetch-solana-authorities.ts

   Alternatively, if you prefer using npx:
       
       npx ts-node --esm fetch-solana-authorities.ts

3. Upon execution, you should see log messages in your terminal that include:
   - Confirmation that the connection to the Solana network is initializing.
   - The network version (proving that the connection was successfully established).
   - Logs for checking the freeze authority, mint authority, and update authority for the specified mint.
   
   Example output:
       Initializing connection to the Solana network using the gsnode.io RPC endpoint...
       Successfully connected to Solana network. Network version: { ... }
       Checking freeze authority for mint: <mint_address>
       Freeze authority for <mint_address>: true
       Checking mint authority for mint: <mint_address>
       Mint authority for <mint_address>: true
       Checking update authority for mint: <mint_address>
       Update authority for <mint_address>: false

Troubleshooting:
----------------
- Ensure that the mint address you provide is a valid base58 string. 
- If you encounter errors related to file extensions or module loading, verify your tsconfig.json and that your package.json includes "type": "module".
- It is recommended to use Node.js LTS (v18) to avoid issues with experimental ESM features.
  
![basic plan](https://github.com/user-attachments/assets/3c5e19ab-40cb-4ef2-89b1-67606e3e6e81)

Additional Information:
-----------------------
See the code in fetching-solana-authorities-typescript.ts join our discord for fast RPCs and gRPC (https://discord.gg/SvUCmXNC)

Also can see more content like this in our web (https://gsnode.io)

Happy coding and exploring Solana!
