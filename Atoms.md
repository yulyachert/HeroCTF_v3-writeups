#Hero CTF
## Atoms

Category | Points 
--- | --- 
Steganography| 50 


- Parts of the string are elements of Mendeleev's periodic table

```
Mt => 109
Md => 101
Ds => 110
Fm => 100
Md => 101
Hs => 108
Md => 101
Md => 101
Uuo => 118
```

- An idea  that these are character codes in ASCII 
- Let's write an exploit that translates the code into a character 
```
const atoms = [109, 101, 110, 100, 101, 108, 101, 101, 118] 
const result = [] 
for (const atom of atoms) {
    result.push(String.fromCharCode(atom).join(""))
} 
console.log(result)
```
- Get a flag

### Flag=Hero{mendeleev}