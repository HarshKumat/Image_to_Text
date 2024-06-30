# Image_to_Text_to_Audio


This Python script allows you to convert text from an image to an audio file. The script uses the `pytesseract` library to extract text from the image and the `gtts` library to convert the extracted text to speech.

## Requirements

- Python 3.x
- `pytesseract` library
- `Pillow` library
- `gtts` library
- Tesseract-OCR

### Installing Tesseract-OCR

Use the package manager to install Tesseract.

```bash
sudo apt-get install tesseract-ocr
```
## Usage
1. Clone the Repository
```
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
```

2. Prepare an Image
Place the image file you want to process in the same directory as the script.

3. Set the Path
Modify the script to include the path to your image file. Example:
```
img_path = "your_image_file.png"
```
4. Execute The Script
     
5. Listen to the Audio
Example: output.mp3

# Script Explanation
## Text Extraction
The script uses the ```pytesseract``` library to extract text from an image:
```
import pytesseract
from PIL import Image

img = Image.open(img_path)
result = pytesseract.image_to_string(img)
```

## Text to Speech Conversion
The script uses the ```gtts``` library to convert the extracted text to speech and save it as an MP3 file:
```
import gtts

tts = gtts.gTTS(result)
tts.save("output_audio.mp3")
```

# License

Feel free to customize this README file further according to your specific project details and needs.

