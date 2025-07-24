Turn your handwritten notes into smart digital summaries.

This project converts handwritten note images into editable digital text using a trained OCR (CRNN+CTC) model, and then automatically cleans and summarizes the content using NLP techniques (e.g. BART summarization). Finally, the output is saved as a searchable, printable PDF.

 Features
 Upload handwritten image

 Extract text using a trained OCR deep learning model

 Auto-clean grammar and summarize with Transformers (facebook/bart-large-cnn)

 Export to searchable PDF

 GUI image selector (no hardcoded paths)

 Perfect for students, professionals, and educators

 Tech Stack
Area	Tech Used
OCR Model	CRNN + CTC (Keras, TensorFlow)
Image Input	OpenCV, Tkinter GUI for file selection
NLP	Hugging Face Transformers (BART Summarizer)
PDF Export	PDFKit

 Folder Structure
bash
Copy
Edit
HandWriting-to-Digital-Notes/
├── ocr_model.h5              # Trained OCR model
├── notebook.ipynb            # Jupyter notebook for running end-to-end process
├── test_image.jpg            # Sample handwritten image
├── temp_note.txt             # Temporary file to convert to PDF
├── digital_note.pdf          # Final digital note (output)
├── README.md                 # You're reading this!
 Installation
1. Clone the repo
bash
Copy
Edit
git clone https://github.com/yourusername/handwriting-to-digital-notes.git
cd handwriting-to-digital-notes
2. Install dependencies
bash
Copy
Edit
pip install tensorflow keras opencv-python pillow transformers pdfkit
 tkinter is built-in with Python (no need to install separately on Windows).
 You also need to install wkhtmltopdf and add it to your system PATH for pdfkit to work.

 Usage
Run the Jupyter notebook:
notebook.ipynb

Click to select an image file of handwritten notes (e.g., .jpg, .png).

The model will:

Predict the text

Clean grammar and summarize

Save it as digital_note.pdf
