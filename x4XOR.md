#Hero CTF
## Record

Category | Points 
--- | --- 
Crypto | 75

- The flag.png.enc is a result of XOR-ing the original flag.png with random key
- The key is 9 bytes long. The first bytes of PNG file are always the same
- Decode the image with a script:
```
from itertools import cycle

def xor(data, key):
    return b''.join((c ^ k).to_bytes(1, 'big') for c,k in zip(data, cycle(key)))

with open("valid.png", 'rb') as input:
    first_9_bytes = input.read(9)
with open("flag.png.enc", "rb") as input:
    encoded = input.read()
    key = xor(encoded[:9], first_9_bytes)
    with open("flag.png", "wb") as output:
        output.write(xor(encoded, key))                          
```
Flag=Hero{123_xor_321}