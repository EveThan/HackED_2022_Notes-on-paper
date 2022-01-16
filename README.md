# This is team 3-Little-Cats-

The project was 

Working on the project at: https://colab.research.google.com/drive/1aYzfO6OQkq7zFwnoKGIVT0d0pxL5ttuq?usp=sharing

Also working at: https://colab.research.google.com/drive/1WMJ6wPWb0A0mwZyL16_OsF6U3sDkQkrc?usp=sharing

Some comments:
- cv2.VideoCapture doens't work on Google Colab. Therefore, code snippets from Google Colab are used to implement the capture photo function. The "Camera Capture" code snippets cosist of two code cells on Google Colab, and can be found by following the following steps:
1. Click "Code snippets" on the menu bar on the left hand side. The symbol of "Code snippets" looks like '< >'.
2. Filter code snippets by typing "Camera Capture" in the search box. 
3. Click "Insert" to insert the code snippets.

- Similarly, cv2.VideoCapture didn't work on Google Colab when I was trying to use it to process live video and capture every frame in the live video. I found code snippets from The AI Guy on YouTube that can achieve this with the help of some JavaScript code. The video can be found at https://www.youtube.com/watch?v=ebAykr9YZ30

- The reason why it's tricky to use the camera on Google Colab is that Google Colab is running on my browser. Hence, some web API's need to be used for Google Colab to access my local hardware such as my camera.
