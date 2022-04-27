# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image using

M=np.float32([[1,0,20],[0,1,50],[0,0,1]])

translated_img=cv2.warpPerspective(input_img,M,(cols,rows))


### Step3:
Scale the image using

M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]])

scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step4:
Shear the image using

M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]])

sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))


### Step5:
Reflection of image can be achieved through the code

M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])

reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))


### Step 6:
Rotate the image using

angle=np.radians(45)

M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])

rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))


### Step 7:
Crop the image using

cropped_img=input_img[20:150,60:230]


### Step 8:
Display all the Transformed images.

## Program:
python
Developed By: P.Sanjay
Register Number: 212220230042

### i)Image Translation

M=np.float32([[1,0,20],
             [0,1,50],
             [0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()



### ii) Image Scaling

M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()

### iii)Image shearing

M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.4,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()


### iv)Image Reflection

M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()


### v)Image Rotation

angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()


### vi)Image Cropping


cropped_img=input_img[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()



## Output:
### i)Image Translation


![1](https://user-images.githubusercontent.com/75235032/165504110-34858eab-eada-43ef-b0f1-b7b4f7b42faa.jpg)

### ii) Image Scaling

![2](https://user-images.githubusercontent.com/75235032/165504119-d8ccca4c-b870-4bca-bdb1-c4d81d2f7844.jpg)



### iii)Image shearing
![3](https://user-images.githubusercontent.com/75235032/165504131-8f02edd8-b041-413e-abe8-c135d56f130d.jpg)


### iv)Image Reflection

![4](https://user-images.githubusercontent.com/75235032/165504146-b6b38a09-f7f0-4146-bee4-b7cc32c49685.jpg)


### v)Image Rotation

![5](https://user-images.githubusercontent.com/75235032/165504151-9db92522-3625-4dd8-afdc-de4ac4f67ec8.jpg)

### vi)Image Cropping
![6](https://user-images.githubusercontent.com/75235032/165504173-b0c9c6ff-91bb-46a6-9551-99ee6111b519.jpg)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
