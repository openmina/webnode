
# The Mina Web Node

The Mina Web Node is a Mina node that can be set up in a matter of seconds and configured through a standard internet browser such as Chrome or Firefox. The Web Node can be run on devices with slow CPUs and low memory. 


## **Try out the Mina Web Node**

Head over to the link below to test out the Berkley net (testnet) version of the Mina Web Node:

[openmina.com](https://openmina.com/)


![image](https://github.com/openmina/webnode/assets/60480123/523dddba-4c03-48db-aa79-543fbd3cf3e0)


Wait until the Web Node has prepared loading inside your browser. The following steps need to be completed first:

**1) Setting up browser for Web Node**

The browser requires a specific environment for the Web Node to run, which is achieved by loading a Web Assembly (wasm) file. As mentioned previously, Web Assembly is a binary instruction format through which we can run code in a browser even if it’s written in languages other than javascript.

**2) Getting ready to verify blocks**

For verifying block SNARKs, we need to fetch a _verifier index_, which contains constants necessary for verifying a block for a given chain.

**3) Connecting directly to Mina network**

The Web Node has to connect directly to the Mina network via WebRTC, without using intermediaries.

**4) Catching up with the network**

The Web Node downloads the latest block and verifies it. In the demo version, this step also fetches the latest state of the demo account along with its[ Merkle proof](https://medium.com/crypto-0-nite/merkle-proofs-explained-6dd429623dc5) from the peer’s ledger. Using the Merkle proof, we can verify that this account state is indeed part of the ledger with the hash that is part of a block we verified.

These four steps should take a total of 15 to 20 seconds. After the Web Node has finished loading, click on the blue button titled **Continue**.


![image](https://github.com/openmina/webnode/assets/60480123/477553c7-f388-491f-a8d6-6e34b5a0d91c)


**Latest block**

Once the Web Node has loaded, it will begin to automatically validate new blocks. In this part of the UI, you can see the number of the latest block verified by your Web Node, as well as the network on which it has been verified. Please note that the current demo version of the Web Node runs on the Berkeley Testnet, but a mainnet version is already in the works.


![image](https://github.com/openmina/webnode/assets/60480123/0edb4009-e53c-44ce-9a64-16c626d92959)


**Account**

Here are the details of your account, which you can also view in the Mina Explorer. In the current testnet version of the Web Node, you are assigned a random pre-funded account.

In the future mainnet version, users will be able to connect their own wallets, and we will strongly recommend that they use a Ledger hardware wallet for this purpose.


![image](https://github.com/openmina/webnode/assets/60480123/969bd32c-5db6-4444-988e-ee6e64a66eba)


**Latest Transaction**

If you have already made a transaction, it will show up in this window after about 4 minutes, which is the time it takes for a block to be produced. You can also verify the confirmation of a transaction in the[ Mina Explorer.](https://minaexplorer.com/)

To make your first transaction, click on the blue button titled **Transfer funds** found in the bottom-right corner of the Web Node’s UI.


![image](https://github.com/openmina/webnode/assets/60480123/e7948de6-4337-410b-b566-d47bcdef234f)


This is the window in which you can input details for sending a transaction. Let’s take a closer look at each section:

![image](https://github.com/openmina/webnode/assets/60480123/d2035ff2-f846-484e-89e4-3ebd6c4fe536)


**Recipient**

Here you enter the wallet address to which you want to send your tMINA funds.

![image](https://github.com/openmina/webnode/assets/60480123/971e194f-c07a-4228-be8e-27b18d0b44f4)


**Amount**

Enter the amount of tMINA you want to send. Please note that the amount plus the fee cannot be higher than the balance of the account assigned to your Web Node.

**Fee**

The fee you wish to pay for the transaction to be processed. The higher the fee, the greater the priority with which your transaction will be processed.


![image](https://github.com/openmina/webnode/assets/60480123/ee41952a-7aeb-4d13-ada7-c82af416e56a)


**Memo (optional)**

If you want to, you can write a memo for your transaction. You can enter up to 32 characters.

Once all details have been inputted and checked, click on the blue **Confirm transaction** button to begin processing the transaction.



![image](https://github.com/openmina/webnode/assets/60480123/85642d07-9fa3-4f9f-ad7e-d6fd128e07e1)


This will take you back to the transaction overview page of the Mina Web Node. In the **Latest Transaction** window, you can see the details of your pending transaction, including the recipient wallet’s address, the amount, the fee as well as the memo you wrote (if any). The transaction will also be allotted a unique Transaction hash.

All of these details can be also viewed on the Mina Explorer by clicking on the **block Explorer** button.

Wait some time (normally up to 4 minutes) until the status of the transaction changes to **Applied**.


![image](https://github.com/openmina/webnode/assets/60480123/0706824d-3a6a-427b-9f26-3965b6104260)


Once the transaction’s status has been changed to Applied, your transaction has been successfully processed, which will reduce your tMINA balance by the sum you sent (plus the transaction fee) and credit the recipient’s wallet by that amount minus the transaction fee. You can confirm this by checking out the transaction in the Mina Explorer by clicking on the[ block Explorer](https://minaexplorer.com/) link found in the upper right corner of the **Latest Transaction** window.

Currently, the Mina Web Node is limited to the Berkeley Testnet. We plan on developing a Mainnet implementation of the Web Node in the future. In the Mainnet version, users will be able to connect their own wallets. We also plan on improving support for smartphones, namely, optimizing the phone’s battery usage and reducing the amount of network IO that needs to be performed.
