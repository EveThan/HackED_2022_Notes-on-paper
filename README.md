# This is team 3 Little Cats

## Team member:
Zheng En (Eve) Than

## Project title:
Notes on Paper

## Worksites:
- This link leads to the notebook where the completed project is: https://colab.research.google.com/drive/1WMJ6wPWb0A0mwZyL16_OsF6U3sDkQkrc?usp=sharing
- My ipynb file is too large to be uploaded to GitHub. 

## Goal:
- To create an interactive program where the program plays a piano key when the user taps on the corresponding key letter on a piece of paper.

## How to use the program:
- Write 7 notes (C, D, E, F, G, A, B) on a piece of paper.
- Show the paper with the 7 letters written on it to the program.
- Take a photo of the paper using the program and check if all letters are recognized well.
- Start the live camera while still showing the paper to the program.
- Tap on any letter on the paper using the tip of index finger. 
- Wait for the program to play the corresponding note. 

## Assumptions:
- The program works under several assumptions. These assumptions can be removed as we enhance the program later on. Due to time constraint in the hackathon, these assumptions are not dealt with yet and they need to be satisfied for the program to work well:
1. Firstly, the environment needs to be well lit or else Google Vision won't be able to recognize the handwriting well.
2. It is recommended to write the letters in bold.
3. The letters need to be apart from each other to avoid the program from reading them as a single word.
4. Each of the 7 letters (C, D, E, F, G, A, B) appear exactly once on the paper. The program doesn't work if a letter is missing. If a letter appears more than once, for example, if there are three 'A' on the paper, only one of the three 'A' will be remembered by the program in terms of its position.

## Possible extension of this functionality:
- I was thinking about my nephew when working on this project. I imagined how fun it would be if, say, my nephew doodled a cat, a bird, and a car on a piece of paper and showed it to a program. When he points at his drawing of a cat, the program recognizes that it is a cat and responds by saying "what a beautiful cat" or playing some sounds. This would certainly encourage my nephew to draw more!

## Additional comments and references:
### Camera
- cv2.VideoCapture doens't work on Google Colab. Therefore, code snippets from Google Colab are used to implement the capture photo function. The "Camera Capture" code snippets cosist of two code cells on Google Colab, and can be found by following the following steps:
1. Click "Code snippets" on the menu bar on the left hand side. The symbol of "Code snippets" looks like '< >'.
2. Filter code snippets by typing "Camera Capture" in the search box. 
3. Click "Insert" to insert the code snippets.

- Similarly, cv2.VideoCapture didn't work on Google Colab when I was trying to use it to process live video and capture every frame in the live video. I found code snippets from The AI Guy on YouTube that can achieve this with the help of some JavaScript code. The video can be found at https://www.youtube.com/watch?v=ebAykr9YZ30

- The reason why it's tricky to use the camera on Google Colab is that Google Colab is running on my browser. Hence, some web API's need to be used for Google Colab to access my local hardware such as my camera.

### Handwriting recognition
- In order to save time, I did not create a machine learning model from scratch and train it to recognize handwritten texts. Instead, I used Google Cloud's Vision API to recognize handwritten words in an image. Google Cloud has offered many tutorials and code samples on their website which helped me immensely. I have used their code sample from https://cloud.google.com/vision/docs/fulltext-annotations. I changed and deleted a few lines of their code since I will only need to recognize words and not blocks and paragraphs.

### Piano key sounds
- The sound files of the 7 piano keys are downloaded from https://freesound.org/people/Tesabob2001/packs/12995/.

### Hand recognition
- A part of the project involves recognizing where my index finger tip is. I referred to https://google.github.io/mediapipe/solutions/hands.html a lot when implementing this function.

### Other references
- I have visited stackoverflow countless times to look for answers for the simplest issues such as how to install a libray on Google Colab.  
