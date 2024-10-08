# Nepali-Handwritten-Character-Recognition

# Introduction-
Devanagari is the national font of Nepal and also used throughout the various part of India. It has 10 numeral characters(०, १, २, ३, ४, ५, ६, ७, ८, ९), 36 consonants (क, ख, ग, घ, ङ, च, छ, ज, झ, ञ, ट, ठ, ड, ढ, ण, त, थ, द, ध, न, प, फ, ब, भ, म, य, र, ल, व, श, ष, स, ह, क्ष, त्र, ज्ञ) and 13 vowels (अ, आ, इ, ई, उ, ऊ, ऋ, ए, ऐ, ओ, औ, अं, अः). Devanagari Characters have some characters with similar structures. The ‘ब’ and ‘व’ are different in only the cross inside circle. Similarly ‘ङ’ and ‘ड’ have only difference is dot. The character ‘प’,’ म ‘, and ‘य’ are almost same. The character ‘२’ and ‘र’ are almost same. Some characters like ‘क्ष’, ‘त्र’, ‘ज्ञ’ are derived from other previous characters like ‘ग’, ‘य’ etc.

# Objectives-
1. To build a web application to recognize Nepali handwritten characters and numerals using CNN and convert the recognized characters in the form of  speech (audio).

# Overview-
1. Image Acquisition
  Uploading Image: Users upload images with black backgrounds and white characters.
  Input through Canvas: Users can draw directly on a digital canvas, with options for single character recognition or word recognition (three separate characters).
2. Preprocessing
  Image Resizing: Standardize input dimensions to 32x32 pixels.
  Normalization: Scale pixel values to 0-1 to ensure uniformity and efficiency in training.
3. Feature Extraction
  Lower-Level Features: Detection of edges, lines, texture patterns, and spatial arrangements.
  Higher-Level Features: Recognition of character components, symmetry, rotation, and global/local features.
4. Classification
  Fully Connected Layer: Converts extracted features into probability scores using the softmax function to identify the most likely character.
5. Output
  Visual Output: Displays recognized characters or words on the screen.
  Text-to-Speech: Converts recognized text into speech for enhanced accessibility, benefiting visually impaired users and children.

# Dataset and Model Training-
Dataset can be downloaded from Kaggle website. Here is the link - https://www.kaggle.com/datasets/rishianand/devanagari-character-set
  1. Focus: Nepali language in the Devanagari script, with 92,000 handwritten images.
  2. Characters: 46 distinct characters (36 consonants, 10 numerals), 2000 images per class.
  3. Image Size: 32x32 pixels.
  4. Handwriting Diversity: Varied styles across different ages and backgrounds.
  5. Dataset Source: CSV file from Kaggle.
  6. Data Split: 80% training (1600 images per class), 20% testing (400 images per class).
  7. Labeling: Characters labeled as character_01_ka, character_02_kha, etc., and numerals as digit_0, digit_1, etc.
  # Encoding Techniques:
  1. Label Encoding: Assigns a unique numerical label to each class.
  2. One-Hot Encoding: Represents each category as a binary vector with a single "1" per row.

# Accuracy of the Model-
1.	Training Accuracy: 0.9914
2.	Validation Accuracy: 0.9837

# Additional Functionality-
1. The model can predict simpler words like कलम, कमल, सरल, घर, etc that doesnot contain any vowel characters and modifiers (ह्रस्व, दीर्घ) by concatenating the individual characters and forming a single word.

# Snapshots of the project-
![Project Screenshot](nhcr.png) 
<p><i>fig 1 : UI interface (Homepage) of the project.</i></p> <br>

![Project Screenshot](nhcr_canvas.png) 
<p><i>fig 2 : Write on canvas feature</i></p> <br>

![Project Screenshot](nhcr_upload.png) <br>
<p><i>fig 3 : Predict by uploading the photo with black background and white text.</i></p> <br>

![Project Screenshot](nhcr_word.png) <br>
<p><i>fig 4 : Word prediction by concatenation of characters.</i></p> <br>
