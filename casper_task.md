# Create and deploy a simple, smart contract with cargo casper and cargo test
Once I created a project with `cargo casper my-project`  
I cd into the contracts folder inside my project. Inside that folder I executed thos commands
```
rustup install $(cat ../rust-toolchain)
rustup target add --toolchain $(cat ./rust-toolchain) wasm32-unknown-unknown
```
Note: The documentation should be updated as the rust-toolchain file is in the root directory ,so I had to changed that otherwise it was giving me errors.

After that I build the project with:
```
cargo build --release
```
Note: After that in order to run the tests I had to move the file `contract.wasm` located in `contracts/target/wasm32-unknown-unknown/release` manually to `tests/wasm` otherwise when i run the command `cargo test` it will fail with following message  
![](https://i.imgur.com/I86lPlu.png)

After moving the `contract.wasm` file manually I got the test working and all passed correctly.
![](https://i.imgur.com/OLxaLUb.png)

# Complete one of the existing tutorials for writing smart contracts

After cloning the github repo and preparing the environment. I followed the tutorial until the end. Finnnally after running `make test` all tests run correctly.
![](https://i.imgur.com/siLTHNW.png)
![](https://i.imgur.com/ZytpWXx.png)
![](https://i.imgur.com/Yk1eCl5.jpg)

# Demonstrate key management concepts by modifying the client in the Multi-Sig tutorial to address one of the additional scenarios

I followed the multi sig tutorial and build the project correctly with:
```
cargo build --release
```
After that I install the NCTL tool and start a network.
```
nctl-assets-setup && nctl-start
```
![](https://i.imgur.com/mIvX6Ez.png)
After that I checked my account:
```
nctl-view-faucet-account
```
![](https://i.imgur.com/1BJxKfn.png)

**Scenario 1: signing transactions with a single key
**

```
npm run start:atomic
```
![](https://i.imgur.com/mNVC15l.png)

# Learn to transfer tokens to an account on the Casper Testnet.

First we need to get the root hash of the node in testnet we want to connect.

![](https://i.imgur.com/dESOZ66.png)

After that I funded an account with 1,000.00000 CSPR.
![](https://i.imgur.com/bwOseCE.png)

You can see in the next two screenshots how i did a transfer through the cli because the deploy_hash matches on the last transaction (I did two transactions).
![](https://i.imgur.com/tAcpWwW.png)
![](https://i.imgur.com/DWwaYvD.png)

# Learn to Delegate and Undelegate on the Casper Testnet

 funded my account with cspr on testnet with the faucet and delegate some cspr and undelegate some. Here are the screenshots:
**Account Public key**
020207a2a646fee8b644f5c3c5ab91402977134f734e056a20e916a9d8d1901ca203

**DELEGATION:**
![](https://i.imgur.com/AfTNeoN.png)

**UNDELEGATION:**
![](https://i.imgur.com/3uANEqY.png)


