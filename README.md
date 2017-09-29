# Proof of Visit
https://f.ruuvi.com/t/proof-of-visit-system-on-ruuvi-and-iota/647

_Everything here is work in progress_

## Description
The goal is to design and build a system to provide a proof that one or several machines (e.g. a user smartphone) has been physically close to a certification device (e,g. a ruuvi tag), recording the information in a blockchain.

This is a very general concept which could be applied in many domains, some of which are:
- prove that two or more parties were together when signing a contract,
- prove that a guardian does a tour of a secured building every night,
- prove that the person providing medical care to a relative did actually visit him or her every day,
- create a rewarding mechanism, e.g. in form of local cryptocurrency, for people visiting your tourist destination, be it a town, a tourist office, or a monument,
- ensure that digital reputation of a place -e.g. a rating on a hotel- is only given by users which have physically being in the place itself in order to avoid fake reviews or comments
disclaimer: Tourism and Hospitality is our use case, visit http://sismotur.com for our background

Simple example of how the system would work:
- 1 the signing device, e.g. a Ruuvi tag, broadcasts a bluetooth signal to show it's open to a connection
- 2 the user opens a dedicated app and launches the signing process by clicking on a button (with a nice UI/UX etc)
- 3a the Ruuvi gives a random string to the smartphone, and gives some seconds to the smartphone to sign it
- 3b the smartphone takes the random string, signs it with its private key, and gives the bundle back to the Ruuvi tag
- 3c the Ruuvi adds a timestamp, wraps the whole message with its own signature, and sends it back to the smartphone
- 3d the smartphone sends the whole message as a transaction block to IOTA and 
- 3e the user gets a final confirmation that the Proof of Visit transaction went OK

_Step 3 is automated_

## Subcomponents
- IoT device that broadcasts a service and signs the Proof of Visit
- Smartphone/IoT device that requests the Proof of Visit
- The syntax and semantics of the message itself
- The system that sends the message to a Blockchain-based system of record
- The Blockchain used to store the messages
- The software -blockchain based or not- used to read and process the messages and do useful things with them
