# 📜 Day 8: Tying it All Together

### ⏱ Agenda

1. [🏆 Learning Objectives](#%F0%9F%8F%86-Learning-Objectives)
2. [📖 [30m] Overview](#%F0%9F%93%96-30m-Overview)
3. [💻 [30m] In Class Activity I](#%F0%9F%92%BB-30m-In-Class-Activity-I)
4. [🌴 [10m] BREAK](#%F0%9F%8C%B4-10m-BREAK)
5. [💻 [30m] In Class Activity II](#%F0%9F%92%BB-30m-In-Class-Activity-II)
6. [📚 Resources & Credits](#%F0%9F%93%9A-Resources--Credits)

## 🏆 Learning Objectives

## 📖 [30m] Overview

### Demo

Go over the main points of the [droxey/rainbowcoin] project, including:

- Truffle boxes, project structure, architectural decisions, technologies used, bugs, truffle commands
- Writing and compiling contracts (`RainbowCoin.sol`, `Migrations.sol`, `Metadata.sol`)
- Creating and running migrations
- Writing and running tests

### Smart Contract Tips & Tricks

## 💻 [30m] In Class Activity I

### Thinking it Through

1. Create a file named `SmartContractNameTest.js` inside of the `test` folder in your project's root directory.
2. In a comment block at the top of the file, write down what capabilities your project's smart contract should have. What does the contract do? **See the below example**:
   ```js
   // 1.
   //
   //
   ```
3. If you finish early, begin working on the second in class activity, where you'll work on implementing these using the Truffle testing framework.

## 🌴 [10m] BREAK

## 💻 [30m] In Class Activity II

### Coding it Up

**Challenge**: Implement each sentence as tests inside `test\SmartContractNameTest.js`.

Use the example file below to help you get started.

**Be sure to replace `YourContractName` with your project's contract name**!

```js
const YourContractName = artifacts.require('./YourContractName.sol');
const _ = '        ';


contract('YourContractName', async function (accounts) {
  let token;

  before(done => {
    (async () => {
      try {
        // TODO: All setup steps belong here, including contract deployment.
        token = await YourContractName.new();
        var tx = await web3.eth.getTransactionReceipt(token.transactionHash);
        totalGas = totalGas.plus(tx.gasUsed);
        console.log(_ + tx.gasUsed + ' - Deploy YourContractName');
        token = await YourContractName.deployed();

        console.log(_ + '-----------------------');
        console.log(_ + totalGas.toFormat(0) + ' - Total Gas');
        console.log(_ + '-----------------------');
        console.log(_ + totalGas.toFormat(0) + ' - Total Gas');
        done();

      }
      catch (error) {
        console.error(error);
        done(false);
      }
    })();
  });

  describe('YourContractName.sol', function () {
    it('Should always pass this canary test', async () => {
      assert(true === true, 'this is true');
    });

    it("Should call another function on your deployed contract", async () => {
      let instance = await YourContractName.deployed();
      // TODO: Write the code here to call a contract function
    });
 });
});
```

## 📚 Resources & Credits

- **[droxey/rainbowcoin]**: The ERC-721 base token as reviewed in class today.


[droxey/rainbowcoin]: https://github.com/droxey/rainbowcoin
