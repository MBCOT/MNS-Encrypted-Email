# MNS (Minima Naming System) / Encrypted Email

The Minima Naming System (MNS) revolutionizes service creation with short, unique names, facilitating encrypted email and payment systems over Maxima. Explore the seamless integration of privacy, decentralization, and financial interactions within the Minima ecosystem.

## Overview

- **Unique MNS Name:** Associate a unique MNS name with any service for easy access and recognition.
- **Encrypted Email:** Secure mailboxes, messages, and access to stored communications.
- **Utilize Maxima's Nodes:** Harness Maxima's distributed nodes to ensure system reliability.
- **Enhance Minima:** Promote privacy, decentralization, and seamless financial interactions.

## Encrypted Email / MNS Over Maxima

### Create Mailbox
- Pick a random entry point to MNS.
- Choose a name for the mailbox, checking availability over Maxima's distributed nodes.
- Create an access token with the user's Maxima public key.
- Link the token ID with the mailbox and the chosen name.
- **Additional Steps:**
  - Access token creation
  - Linking token ID

### Send a Message
- Pick a random entry point to MNS.
- Ask MNS to locate a mailbox name.
- Retrieve the public key of the destination mailbox.
- Encrypt the message using the mailbox's public key.
- Send the Maxima message with the mailbox name and the encrypted message.
- **Additional Steps:**
  - Message encryption
  - Message distribution by nodes

### Retrieve Stored Message
- Pick a random entry point to MNS.
- Ask MNS to locate a mailbox name.
- Request access to the mailbox.
- Execute a handshake protocol between the server and the user over Maxima.
- Decrypt stored messages using the user's Maxima private key.
- **Additional Steps:**
  - Handshake protocol
  - Decryption options

## Additional Features
- **Option 1:** Decrypt messages on the client side using the MNS Dapp.
- **Option 2:** Forward stored messages to the user's Maxima address.

## Conclusion

By creating an MNS system over Maxima, users gain access to encrypted email, transactions, and payments with simple names and cryptographically secure methods. This system enhances the Minima ecosystem, fostering growth and innovation in decentralized communication and financial interactions. Join us in shaping the future of Minima with enhanced privacy, security, and usability.

## Notes

- Distributed / replicated DB over the Nodes that makes MNS network over Maxima.
- MNS entry point: A maxima address to a Node of the MNS network to reach other nodes of the network.
  - The MNS network pulishes on chain on a contract, a random list of a few entry point, this list would be refresh every few hours.
    
- The MNS network does not requires that every node has a permanent Maxima Address, only a part of the Network would have Maxima permanent address and some of them would be published on chain every few hours to avoid attacks.
  The other nodes of the network would be connected between them as Contacts, making a kind of mesh network
- Mailbox: It is a record on a DB with an unique name choosen by a user that stores Maxima messages sent by any user encrypted with the Maxima publickey of the owner of the mailbox.
  - Security: As any information to be stored on the mailbox would come thru Maxima, and the message itself will be encrypted from the origin with the Maxima publickey of the owner of the mailbox, it is a robust and safe system to be used on a distributed or replicated DB.
    
- Hand Shake Protocol:
  - The server give the Maxima address to contact to him to the user and a random number.
  - The user send a Maxima message to the server with the random code received.
  - The server checks that the publickey of the mailbox is the same from the Maxima message received from the user and also checks the random code.
  - The server grants access to the functionality asked.
