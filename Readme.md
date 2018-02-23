﻿# AESClass
AESClass is a lightweight class for encrypting and decrypting with AES

You can encrypt or decrypt byte[], base64-strings or normal strings to your favorite output type. 

## Facts

- .NET native AES-Implementation
- Hardcoded Keysize 256 / Blocksize 128
- PBKDF2 Padding with random iteration (adjustable)
- Random IV

## EncryptedPaket-Structure

| Offset | Length | Type | Description |
| --- | --- | --- | --- |
| `0x00` | 4 bytes | Int32 | PBKDF2-Iterations |
| `0x04` | 16 bytes | byte[] | InitialVector *(autogenerated)* |
| `0x14` | 64 bytes | byte[] | Salt *(autogenerated)* |
| `0x54` | n bytes | byte[] | Encrypted data |

### Hint

**I'm using elements of C# 6.0. Be sure your compiler is configured for C# 6.0**

**Dev-Website:** http://par0noid.info