#Hero CTF
## Ping Pong

Category | Points 
--- | --- 
Prog | 45 

- Download output.txt file
- Replace PONG with a 0 and PING with a 1
- Now we have a binary sequence

```
0100100001100101011100100110111101111011011100000011000101101110001101100
1011111011100000011000001101110001101100101111100110001001101010101111101
100110011101010110111001111101
```
- Run exploit and get the flag
```
result = ""
with open("output.txt", "r") as file:
    for str in file:
        if str == "PONG\n":
            result += "0"
        elif str == "PING\n":
            result += "1"
        else:
            print(str)
print(str)
```

### Flag=Hero{p1n6_p0n6_15_fun}