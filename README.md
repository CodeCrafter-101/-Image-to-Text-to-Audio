# Image to Text to Audio


- ###  "Image to Text to Audio" is a pipeline-based application that extracts text from an image and converts that extracted text into spoken audio. This project combines computer vision (OCR), natural language processing, and text-to-speech synthesis.The script uses the pytesseract library to extract text from the image and the gtts library to convert the extracted text to speech.**



## Objective

Transform any image containing text (e.g., signboards, handwritten notes, documents) into audible speech to enhance accessibility and usability.  


## Requirements

- Python 3.x
- `pytesseract` library – for Optical Character Recognition (OCR)
- `Pillow` library – for image handling
- `gtts` library
- Tesseract-OCR



## You also need to install Tesseract-OCR - 
Use the package manager to install Tesseract: sudo apt-get install tesseract-ocr



## Project Structure
![image](https://github.com/user-attachments/assets/abd205c5-adec-4d9f-a660-aff34fb18174)



## How It Works

1. Image Input
- Load an image that contains visible and readable text.
2. OCR (Optical Character Recognition)
- Use pytesseract to extract text from the image.
3. Text Preprocessing (optional)
- Clean or format the text if needed (e.g., punctuation, case).
4. Text-to-Speech
- Convert the text into audio using gTTS or pyttsx3.
5. Audio Output
- Save the audio to a file and optionally play it.

  
## Text Extraction

The script uses the pytesseract library to extract text from an image:
- result = pytesseract.image_to_string(img)



## Text-to-Speech Conversion
The script uses the gtts library to convert the extracted text to speech and save it as an MP3 file:
-tts = gtts.gTTS(result)
tts.save("output_audio.mp3")
