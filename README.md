# OCR Web App

This repository provides a simple Flask application that lets you upload an image, preview it, and extract text using Tesseract OCR. The extracted text can be copied to your clipboard from the browser.

## Requirements

- Python 3
- Flask
- Pillow
- pytesseract
- Tesseract OCR installed on your system

Because this environment is offline, the required packages are not included. Install them using pip and ensure that the `tesseract` binary is available on your PATH.

```
pip install Flask Pillow pytesseract
```

## Running the Application

1. Install the dependencies listed above.
2. Run the application:

```
python app.py
```

3. Open `http://localhost:5000` in your browser.
4. Upload an image, preview it, and click **Extract** to display the text. Use the **Copy** button to copy the text to your clipboard.
5. Uploaded images are stored in `static/uploads`.

## Note

If you wish to use an external OCR service (such as Azure Cognitive Services), replace the call to `pytesseract.image_to_string` in `app.py` with your API call of choice.
