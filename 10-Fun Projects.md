# 10. Fun Projects

## Summary
Let's try some things!

## Generate a QR Code
```sh
$ pip3 install qrcode
```
```py
import qrcode

img = qrcode.make("https://www.youtube.com/")
img.save("youtubeQR.jpg")
```
## Read a QR Code
```sh
$ pip install opencv-python
```
```py
import cv2

d = cv2.QRCodeDetector()
val, _, _ = d.detectAndDecode(cv2.imread("myQRCode.jpg"))
print("Decoded text is: ", val)
```

## More projects!
Just hit up Google or your favorite search engine! Here's a good list on geeksforgeeks.org: [https://www.geeksforgeeks.org/python-projects-beginner-to-advanced/](https://www.geeksforgeeks.org/python-projects-beginner-to-advanced/)

---
[Prev: Pip & Modules](<9-Pip & Libraries.md>)