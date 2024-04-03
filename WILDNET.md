Wildnet is a Monero testnet with many limits either relaxed greatly or removed outright.
It is based off of stagenet, and intended for experimentation purposes.

Wildnet changes (so far):
* Changed transaction output limits:
    * Decreased minimum: 2 -> 1
* Changed ringsize limits:
    * Decreased minimum: 16 -> 1
    * Removed maximum: 16 -> N/A
    * No longer require uniform ringsize across rings
* Changed mandatory output lock times:
    * Decreased non-coinbase lock time: 10 blocks -> 1 block

Roadmap:
* Increase maximum transaction outputs: 16 -> ???
* Increase maximum transaction size: 1 MB -> ???
* Increase penalty-free block size: 300 KB -> ???
* Increase TX_EXTRA size limit: 1060 bytes -> ???
* Decrease coinbase lock time: 60 blocks -> 1 block
* Re-enable old transaction types

TODO:
* Add wildnet to ./src/checkpoints/checkpoints.cpp
* Add wildnet to ./src/p2p/net_node.inl
* Add wildnet to get_approximate_blockchain_height() in ./src/wallet/wallet2.cpp
* Add wildnet to ./tests/functional_tests/validate_address.py
* Add wildnet to ./translations/*