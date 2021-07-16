# Video-Face-Detection
## Python Code:
### import cv2   
### Load the cascade  
face_cascade = cv2.CascadeClassifier('haarcascade_frontalface_default.xml')  
  
### To capture video from existing video.   
cap = cv2.VideoCapture('test.mp4')  
  
### In while loop :
### Read the frame  
 _, img = cap.read()  
  
### Convert to grayscale  
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)  
  
### Detect the faces  
faces = face_cascade.detectMultiScale(gray, 1.1, 4)  
  
### Draw the rectangle around each face  
for (x, y, w, h) in faces:  
cv2.rectangle(img, (x, y), (x+w, y+h), (255, 0, 0), 2)  
  
### Display  
cv2.imshow('Video', img)  
  
### Stop if escape key is pressed  
 k = cv2.waitKey(30) & 0xff  
 if k==27:  
 break 
          
### Release the VideoCapture object  
cap.release()  
## Picture From The Result : 
![scve](https://user-images.githubusercontent.com/67175109/126001646-917ad265-a1be-4545-9ba9-926ca8bbfe6b.PNG)
![vsdc](https://user-images.githubusercontent.com/67175109/126001666-477ea1fa-5272-4e60-b427-6751d62d4e80.PNG)
![vzesa](https://user-images.githubusercontent.com/67175109/126001669-8d6fbb4c-9222-4a3b-abaf-124189bcb376.PNG)

          

