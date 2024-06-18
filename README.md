# Simple BLS

This project demonstrates a basic Hardhat and typescript approach to signing data offchain and having it verified with bls signatures on chain. 

Make sure your env matches the .example.env 

```shell
npm i 
npx hardhat compile 
npx hardhat run script/deploy.ts --network holesky 
source .env 
npx hardhat verify $BLS_CONTRACT_ADDRESS --network holesky 
npx ts-node crypto/generate_registration_data.ts
npx hardhat run script/register.ts --network holesky 
```

Missing from this project: 

- BLS apk caching optimizations 
- Deregistering 
- Verifying some APK is a subset of the contract APK 
- Voting power 
- More robust domain hash conforming to EIP712 
