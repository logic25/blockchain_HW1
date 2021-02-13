<p align="left">
    <ins><b>Zbank - Blockchain POA Project</b><br><ins><br>
</p>
<p>

We will be utilizing Geth to create a blockchain as a tool for Zbanks customers. Setup instructions and Dependicies are listed below:  

- Geth
- MyCrypto
</p></br>
 
<img src=Screenshots/Capture1.png><br>
1. In the image above we used the datadir flag to specify the directory of node1 and then node2 and generate the required keys. It is strongly suggested that you copy and paste these keys into a document as we will need them later on. Each node that was created is password protected (node1=1234, node2=12345). These passwords have been placed in a text file and will be recalled later on.Once completed you will hit "Enter"

<img src=Screenshots/Capture2.png><br>
2. Here we can see that we used the Puppeth CLI (command line interface) to create the Ethereum network we named cryptomoney using the Proof of Authority consenses algorithim. Once completed you will hit "Enter" and then select option 2 from the next prompt which will allow the configuration of a new genesis. The next prompt select option 1 to create a new genesis. The final prompt in this section asks which consenses engine you will want to use and we went with option 2.

<img src=Screenshots/Capture3.png><br>
3. We've decided that the duration block should take should be 1 sec. In the next two prompts you will need to paste in (told you that you were going to need it) the public keys generated for each of the nodes above and then exported our genesis configuation and finally set the chain id was set to 2021. 

<img src=Screenshots/Capture4.png><br>
<img src=Screenshots/Capture5.png><br>
<img src=Screenshots/Capture6.png><br>
<img src=Screenshots/Capture7.png><br>
4. Then using the geth flags allow-insecure-unlock (which allows the node to be unlocked) and our pub key from node1 we began to mine the first node. That node produced the enode which we need to copy and paste for use later when we go to run the second node.<br>
<br>
In a new window we ran the same code we used above to now start mining the second node but also added the bootnode flag to connect this node2 to node1 using the enode link from node1.<br>
<img src=Screenshots/Capturemycrypto.png><br>
<img src=Screenshots/Capturemycrypto2.png><br>
<img src=Screenshots/Capturemycrypto3.png><br>
Now we will connect to a new wallet using MyCrypto. In mycrypto click on change network and then scroll down and click on add custom node. Here you will type the name of node, we used the cryptomoney as the node name, then the dropdown box you want to select custom, in the next field you'll type the name of your network (cryptomoney), in the currency field set the currency to ETH, in the Chain ID field enter the chain ID 2021 and finally in the url enter http://127.0.0.1:8545 and then click save and use custom node.
<br>
<img src=Screenshots/Capture8.png><br>
Horray!!! We now have connected to our wallet. <br>
<img src=Screenshots/Capture9.png><br>
We will now test sending funds. 
<img src=Screenshots/Capture10.png><br>
<img src=Screenshots/Capture11.png><br>
We have confirmed that the transactions have been sent successfully.
