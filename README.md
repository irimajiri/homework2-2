# homework2-2

import cv2

capture = cv2.VideoCapture(0)

while(True):
    ret, frame = capture.read()
    cv2.imshow('frame1',frame)  //処理なしの画像
    cv2.imshow('frame3',cv2.cvtColor(frame, cv2.COLOR_RGB2HSV)) //hsv変換した画像  
    if cv2.waitKey(1) & 0xFF == ord('q'): //qを押したら終了.
        break

capture.release()
cv2.destroyAllWindows()




//Python 3.6.6 |Anaconda custom (64-bit)| (default, Jun 28 2018, 11:07:29) 
//[GCC 4.2.1 Compatible Clang 4.0.1 (tags/RELEASE_401/final)] on darwin
//Type "help", "copyright", "credits" or "license" for more information.


//色調変換としてhsv変換を行った.
//YOUTUBE:https://www.youtube.com/watch?v=32sx4dq0bhk&feature=youtu.be
