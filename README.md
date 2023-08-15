<h1 align="center">Digital Signature</h1>


## About the library
The library contains contains RSA digital signature algorithm

## Class RSASignature: 

### Constructors: 
- **RSASignature(BigInteger p, BigInteger q, BigInteger privateexp, CryptoHash hashFunction)** 
  - p,q - prime number
  - privateexp - private exponent, 1 < p < (p-1)(q-1), gcd(privateexp, (p-1)(q-1)) = 1, 
  - hashFunction - The object to get the hash function (Must implement the interface CryptoHash)
     

### Methods: 
- **BigInteger sign(byte[] message)** - Sign an array of bytes
  - return signature = hash(message)^d mod r


- static boolean checkSignature(RSAPublicKey key, BigInteger signature, byte[] message, CryptoHash hashFunction) - Verifies signature validity



