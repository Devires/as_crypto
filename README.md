# as_crypto
A plsql implementation of some functions/procedures in dbms_crypto

## Improvements over Original Version
This version adds a new function to verify a token using public key's Modulus and Exponent, useful to work with JWKS endpoints that exposes only "n" and "e" features of the public key, and not provides the PEM format:

```
  function verify( src raw
                 , sign raw
                 , pub_key_n raw
                 , pub_key_e raw
                 , pubkey_alg binary_integer
                 , sign_alg binary_integer
                 )
  return boolean;
```
