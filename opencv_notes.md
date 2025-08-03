```python
import cv2

# Read the image from directory
image = cv2.imread("image.jpg") 
# we need to pass path as argument

# Blur the image
# Argument - Kernal Size (ksize) for intensity of blur
blurred = cv2.blur(image, (50, 50))

# Write the image to directory
# Arguments 2 required
# Output file name, image to write
cv2.imwrite("test.png", blurred)

# Crop the image and display it
# opencv does not crop support crop option on image directly, we can slice it to another image variable
# sliced_image = image[x1:y1, x2:y2]
sliced_image = image[240:450, 680:900]

# Read and process video file
videocapture = cv2.videoCapture("video.mov")

while videocapture.isopened():
    # intialize variable success, frame (input frame from video)
    # videocapture.read provide two outputs

    success, frame = videocapture.read()
    if success:
        # display frame
        cv2.imshow("test", frame)
        if cv2.waitkey(2) & 0xFF == ord("q"):
            break
    else:
        break # break the window one frames

        
# Visualize the image
# Argument 2 required
# window name and image
cv2.imshow("test", blurred)

# Display untill key press
cv2.waitkey(0)

```

