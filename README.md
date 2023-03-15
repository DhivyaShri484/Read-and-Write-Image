# READ AND WRITE AN IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.
i) Read, display, and write an image.
ii) Access the rows and columns in an image.
iii) Cut and paste a small portion of the image.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
## Program:
### Developed By:
### Register Number: 
i) #To Read,display the image
```
import cv2
from google.colab.patches import cv2_imshow
a = cv2.imread('/content/APPLELOGO.jpg',1)
cv2_imshow(a)
cv2.waitKey(0) 
```
ii) #To write the image
```
colorImage = cv2.imread('/content/APPLELOGO.jpg',1)
cv2.imwrite('written.jpg',colorImage)
writtenImage = cv2.imread('written.jpg',1)
cv2_imshow(writtenImage)
cv2.waitKey(0)
```
iii) #Find the shape of the Image
```
colorImage = cv2.imread('/content/APPLELOGO.jpg',1)
print(colorImage.shape)
```
iv) #To access rows and columns
```
import random
colorImage = cv2.imread('/content/APPLELOGO.jpg',1)
for i in range(100):
    for j in range(colorImage.shape[1]):
        colorImage[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)]
cv2_imshow(colorImage)
cv2.waitKey(0)
```
v) #To cut and paste portion of image
```
color_img = cv2.imread('/content/APPLELOGO.jpg',1)
tag = color_img[200:400,300:500]
color_img[200:400,100:300] = tag
cv2_imshow(color_img)
cv2.waitKey(0)
```

## Output:

### i) Read and display the image
![image](https://user-images.githubusercontent.com/94505585/225331821-a252d6cc-d770-4b7a-9726-39678b1811a4.png)


### ii)Write the image
![image](https://user-images.githubusercontent.com/94505585/225331877-dc59cef3-2a91-48f7-a0a0-9fb7f6874414.png)


### iii)Shape of the Image
<img width="285" alt="image" src="https://user-images.githubusercontent.com/94505585/225332039-9ba95204-af71-4e5d-9218-5d5b01739965.png">


### iv)Access rows and columns
![image](https://user-images.githubusercontent.com/94505585/225332094-c2f7f521-194f-4c06-8782-95289d465139.png)


### v)Cut and paste portion of image
![WhatsApp Image 2023-03-15 at 7 25 03 PM](https://user-images.githubusercontent.com/94505585/225332309-b081fe76-4bd4-46f5-be37-1f5a45a3ebe7.jpeg)


## Result:
Thus the images are read, displayed, and written successfully using the python program.


