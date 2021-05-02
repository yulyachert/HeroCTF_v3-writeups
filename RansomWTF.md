#Hero CTF
## RansomWTF

Category | Points 
--- | --- 
stenography | 60

- Look at the picture. Mixed up pixels can be seen. Thus, we have to put them back in place
- A random seed is 420. The size of the picture is 1280x720, so we have to use an array with elements from 0 to 1280
- Write a script that mixed up everything and then puts pixels back in place, the result has to be written back into the picture
```
np.random.seed(420)
size = 1280
img = cv2.imread(image)
img_arr = np.asarray(img)
for i in range(img_arr.shape[0]):
    indexes = list(range(size))
    np.random.shuffle(indexes)
    arr = img_arr[i]
    res = [0] * size
    for j, index in enumerate(indexes):
        result[index] = arr[j] 
    img_arr[i] = np.array(res)  
gray_color = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
cv2.imwrite(‘image.jpg', gray)
```

### Flag=Hero{S3eD3d_Scr4Mbl3}