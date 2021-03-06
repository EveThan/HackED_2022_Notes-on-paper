# Notes on Paper: Play piano by tapping on your paper
## HackED 2022: Winner of Best use of Google Cloud
<a href="https://devpost.com/software/notes-on-paper" target="_blank"><strong>Notes on Paper on Devpost</strong></a>

<br>

This image is obtained from running the last cell in <a href="https://colab.research.google.com/drive/1WMJ6wPWb0A0mwZyL16_OsF6U3sDkQkrc?usp=sharing" target="_blank">Notes on Paper on Google Colab</a>.
<p align="center">
  <img src = "https://user-images.githubusercontent.com/46462603/150085986-a0122580-be7c-4ca5-9367-2bb26f142de3.jpeg">
</p>          

<br>

## Goal 🎯
To create an interactive program where the program plays a piano key when the user taps on the corresponding key letter on a piece of paper.

## Code, files, or folders needed to run the program 📁
- <a href="https://colab.research.google.com/drive/1WMJ6wPWb0A0mwZyL16_OsF6U3sDkQkrc?usp=sharing" target="_blank">Notes on Paper on Google Colab</a>
- <a href="https://github.com/ZhengEnThan/Notes-on-paper/tree/main/Sounds" target="_blank">Sounds</a>
- key.json file which contains my credentials to connect to Google Cloud

The Notes on Paper ipynb file is too large to be uploaded to GitHub. It may look like the code cells in the file are out of order. They are arranged in that way to make demonstrating the project for HackED 2022 easier. With all the previous code cells already run, simply run the code cells after the title 'Demo for HackED 2022' one by one to do a demo. 

## How to use the program ❓
- Write 7 notes (C, D, E, F, G, A, B) on a piece of paper.
- Show the paper with the 7 letters written on it to the camera.
- Take a photo of the paper using the program and check if all letters are recognized well.
- Start the live camera while still showing the paper to the program.
- Tap on any letter on the paper using the tip of index finger. 
- Wait for the program to play the corresponding note. 

## What have I learned 📚
- Explored code snippets available on Google Colab to implement functions such as capturing photo on Google Colab.
- Explored and used code snippets to process live video and capture every frame in the live video on Google Colab. 
- Used Google Cloud Vision API with the dense document text detection feature to recognize handwritten texts in photos.
- Used the MediaPipe Hands module to recognize and locate hands and fingers in a live video. 
- Used the Ipython.display.Audio module to play sounds on Google Colab.

## Main libraries or modules used 🧩
- google.cloud.vision 
- mediapipe
- cv2
- PIL
- IPython.display
- numpy

## Assumptions ✅
The program works under several assumptions. These assumptions can be removed as we enhance the program later on. Due to time constraints in the hackathon, these assumptions or criteria are not dealt with yet and they need to be satisfied for the program to work well:
1. Firstly, the environment needs to be well lit or else Google Vision won't be able to recognize the handwriting well.
2. It is recommended to write the letters in using a dark-colored pen. It is better to have the letters written in bold.
3. The letters need to be apart from each other to avoid the program from reading them as a single word.
4. Each of the 7 letters (C, D, E, F, G, A, B) appears exactly once on the paper. The program doesn't work if a letter is missing. If a letter appears more than once, for example, if there are 3 'A' on the paper, only one of the 3 'A' will be remembered by the program in terms of its position.

## Possible extension of this functionality 🚀
I was thinking about my nephew when working on this project. I imagined how fun it would be if, say, my nephew doodled a cat, a bird, and a car on a piece of paper and showed it to a program. When he points at his drawing of a cat, the program recognizes that it is a cat and responds by saying "what a beautiful cat" or playing some sounds. This would certainly encourage my nephew to draw more!

## Approaches and references 💬
### Camera 📷
cv2.VideoCapture doens't work on Google Colab. Therefore, code snippets from Google Colab are used to implement the capture photo function. The "Camera Capture" code snippets cosist of two code cells on Google Colab, and can be found by following the following steps:
1. Click "Code snippets" on the menu bar on the left hand side. The symbol of "Code snippets" looks like '< >'.
2. Filter code snippets by typing "Camera Capture" in the search box. 
3. Click "Insert" to insert the code snippets.

- Similarly, cv2.VideoCapture didn't work on Google Colab when I was trying to use it to process live video and capture every frame in the live video. I found code snippets from The AI Guy on YouTube that can achieve this with the help of some JavaScript code. The video can be found on YouTube: <a href="https://www.youtube.com/watch?v=ebAykr9YZ30" target="_blank">Real-time YOLOv4 Object Detection on Webcam in Google Colab | Images and Video</a>.

- The reason why it's tricky to use the camera on Google Colab is that Google Colab is running on my browser. Hence, some web API's need to be used for Google Colab to access my local hardware such as my camera.

### Handwriting recognition ✍🏻
- In order to save time, I did not create a machine learning model from scratch and train it to recognize handwritten texts. Instead, I used Google Cloud's Vision API to recognize handwritten words in an image. Google Cloud has offered many tutorials and code samples on their website which helped me immensely. I have used their code sample from the <a href="https://cloud.google.com/vision/docs/fulltext-annotations" target="_blank">dense document text detection tutorial</a>. I changed and deleted a few lines of their code since I will only need to recognize words and not blocks and paragraphs.

### Piano key sounds 🎹
- The piano keys used are the 7 white keys from C4 to B4.
- The sound files of the 7 piano keys are downloaded from <a href="https://freesound.org/people/Tesabob2001/packs/12995/" target="_blank">Freesound</a>. 

### Hand recognition ✋
- A part of the project involves recognizing where my index finger tip is. I referred to <a href="https://google.github.io/mediapipe/solutions/hands.html" target="_blank">MediaPipe Hands</a> a lot when implementing this function.

~ Project created in January 2022 ~
