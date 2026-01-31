# Falcon 512 vectors

The `falcon512-KAT.rsp` contains 10,000 examples of signatures created by the falcon submission package found at https://falcon-sign.info/falcon-round3.zip

The KAT generation was modified to generate 10,000 examples instead of 100, and to sign messages that are 32-bytes in length.


Each entry has the following form:

- `count` - the index of the entry
- `seed` - a random seed used for the generating the entry (hexadecimal)
- `mlen` - the length of the message (e.g. 32 implies 32 bytes)
- `msg` - the message to be signed (hexadecimal)
- `pk` - the public key of the signer (hexadecimal)
- `sk` - the secret key of the signer (hexadecimal)
- `smlen` - the length of `sm`
- `sm` - first two bytes are the length of the signature, followed by a 40-byte salt, followed by `msg` followed by the signature itself
