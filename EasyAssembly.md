#Hero CTF
## Easy Assembly

Category | Points 
--- | --- 
Rev | 40 

1. Open the code on the website https://godbolt.org/ 
2. Look at the lines 
```
modified = input >> 2;
if (modified == 1337404) 
```
4. We understand that `input = modified * 4`, and `modified = 1337404` 
5. Look at the line `Well done! You can validate with the flag Hero {% d:% d} \ n ", input, modified)`, 
enter the appropriate numbers and get the flag

### Flag=Hero{5349616:1337404}