<p align="center">
  <a href="" rel="noopener">
 <img width=200px height=200px src="https://avatars.githubusercontent.com/u/173536817?s=200&v=4" alt="Project logo"></a>
</p>

<h3 align="center">Translating Old Persian cuneiform by artificial intelligence (AI)</h3>

<div align="center">

  [![Status](https://img.shields.io/badge/status-active-success.svg)]() 
  [![GitHub Issues](https://img.shields.io/github/issues/kylelobo/The-Documentation-Compendium.svg)](https://github.com/Electronic-Old-Persian-Library/Old-Persian-Cuneiform-OCR/issues)
  [![GitHub Pull Requests](https://img.shields.io/github/issues-pr/kylelobo/The-Documentation-Compendium.svg)](https://github.com/Electronic-Old-Persian-Library/Old-Persian-Cuneiform-OCR/pulls)
  [![License](https://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)

</div>

---

<p align="center">An OCR model was developed to translate Old Persian texts into modern languages, utilizing diverse global data sources and training with EasyOCR.
    <br> 
</p>

## 📝 Table of Contents
- [About](#about)
- [Getting Started](#getting_started)
- [Deployment](#deployment)
- [Usage](#usage)
- [Built Using](#built_using)
- [TODO](../TODO.md)
- [Contributing](../CONTRIBUTING.md)
- [Authors](#authors)
- [Acknowledgments](#acknowledgement)

## Abstract  <a name = "abstract"></a>
In this project, I developed an optical character recognition (OCR) model to decipher Old Persian language to modern languages. The process of converting an image text to machine-readable text is called OCR. To the best of my knowledge, I am the first one who is developing this language in this scale in the world. The primary raw data is collected from all over the world. For instance, the British museum collection, cuneiform digital library Initiative (CDLI), Livius and my personal photography from the national museum of Iran and Takht-e-Jamshid (Persepolis). I have trained my data with some OCR models, the best one is based on the EasyOCR model.

## Introduction <a name = "introduction"></a>
Saving the history of my country, Iran, is a very important and valuable issue that we have to care about. The history that we have nowadays is our ancestor’s heritage that we must transfer to the next generations. In this regard, deciphering ancient cuneiforms has been one of the difficult challenges during the span of time to figure out how our ancestors could live in this world. One day, I was thinking, if there is no one in this world who can translate the Old Persian language, what will happen to this language?! How will the next generation decipher new found inscriptions or tablets?! So, this new brainstorm crosses my mind to develop a new AI model to achieve this goal and keep this ancient language alive forever.

## Previous research <a name = "introduction"></a>
Saving the history of my country, Iran, is a very important and valuable issue that we have to care about. The history that we have nowadays is our ancestor’s heritage that we must transfer to the next generations. In this regard, deciphering ancient cuneiforms has been one of the difficult challenges during the span of time to figure out how our ancestors could live in this world. One day, I was thinking, if there is no one in this world who can translate the Old Persian language, what will happen to this language?! How will the next generation decipher new found inscriptions or tablets?! So, this new brainstorm crosses my mind to develop a new AI model to achieve this goal and keep this ancient language alive forever.

## Developing models
I have developed three OCR models in this project:

- yolo_cnn_old_persian

- tessearct_old_persian

- easyocr_old_persian

I have developed an “easyocr_old_persian” model from scratch and trained it with 42 images of the last 12 lines of the great Darius’s inscription in Persepolis, DPd inscription as primary data. This model deciphers Old Persian cuneiform to English transcription and is published on the Old-Persian-Cuneiform-OCR repository on Github. This repository is a part of Electronic Old Persian Library (EOPL) organisation. Since I was looking for an OCR model for Old Persian language, I have not implemented image pre-processing for my models yet and they work on just black and white images. Additionally, my models are still under developing. In the future I will train the “easyocr_old_persian” model with more real data to get better results.

The “tessearct_old_persian” model is a pre-trained model and developed by S. Muhammad Hossein Mousavi. I just developed a code for evaluating this pre-trained model by Python programming language.

The “yolo_cnn_old_persian” model is not completed yet.

## Results and discussion

## Future work
- Developing pre-processing for the raw image dataset

- Training “easyocr_old_persian” model with huge images

- Developing NLP models to translate English transcriptions to modern Persian
  
## Conclusion
Acquired results of the evaluation indicate that my models will be able to properly translate Old Persian cuneiform. The acquired results are promising that they are able to make and improve NLP in this area.

## References
<a id="1">[1]</a> 
Mostofi, Fahimeh. (2014). Intelligent Recognition of Ancient Persian Cuneiform Characters. 10.5220/0005035401190123. 
<br>
<a id="2">[2]</a> 
Mousavi, Seyed & Lyashenko, Vyacheslav. (2017). Extracting old persian cuneiform font out of noisy images (handwritten or inscription). 241-246. 10.1109/IranianMVIP.2017.8342358. 
<br>
<a id="3">[3]</a> 
Gutherz, Gai & Gordin, Shai & Sáenz, Luis & Levy, Omer & Berant, Jonathan. (2023). Translating Akkadian to English with neural machine translation. PNAS Nexus. 2. 10.1093/pnasnexus/pgad096. 

## 🚀 Deployment
```bash
!pip install pytesseract
!apt-get install tesseract-ocr
!pip install pillow
%cd /usr/share/tesseract-ocr/4.00/tessdata/
!mv /content/drive/MyDrive/Persiancuneiform1/tesseract/myLang.traineddata /usr/share/tesseract-ocr/4.00/tessdatafrom PIL import Image
import pytesseractpytesseract.pytesseract.tesseract_cmd = r’/usr/bin/tesseract’img_path =’/content/drive/MyDrive/Persiancuneiform1/DPd.png’
img = Image.open(img_path)
text = pytesseract.image_to_string(img, lang=’myLang’)
print(text)
```

## ✍️ Authors <a name = "authors"></a>
- [@kylelobo](https://github.com/kylelobo) - Idea & Initial work
See also the list of [contributors](https://github.com/kylelobo/The-Documentation-Compendium/contributors) who participated in this project.

## 🎉 Acknowledgements <a name = "acknowledgement"></a>

