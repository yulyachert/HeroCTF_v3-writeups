#Hero CTF
## Russian Doll

Category | Points 
--- | --- 
Misc | 50 

1. Obviously our flag is too deep in the archive
2. In the terminal go to the unzipped archive
3. Write the ls -R command to recursively search for all files
4. We see that there is flag.txt at the end
5. Copy the path
6. Print `cd "copied path"`, so go to the directory with the flag
7. Print `cat flag.txt`
8. Get the flag

### Flag=Hero{if_yOu_gOt_HEre_By_clIcKInG_mANnUaLly_YoU_sHOuLd_REalLy_SeE_SoMeOne}