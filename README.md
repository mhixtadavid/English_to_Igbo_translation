# Customer Service-Focused Translation System: English to Igbo for the Retail Sector

## Project Overview
This project is a customer service-focused translation system designed to translate text from English to Igbo, specifically tailored for the retail sector in Nigeria. The system is built using supervised learning techniques and machine translation models to ensure accuracy and contextual relevance in translations, with a strong emphasis on handling the complexities of the Igbo language, including its tonal nature and cultural idioms.

By integrating this system into customer service platforms, businesses can better serve their Igbo-speaking customers, improving overall customer satisfaction and fostering inclusivity in Nigeria's multilingual retail environment.

## Features
- **Accurate Translations**: The system provides translations from English to Igbo, accounting for cultural and linguistic nuances.
- **Supervised Learning**: Trained on a large dataset of English-Igbo translation pairs.
- **Real-Time Translation**: Capable of handling real-time customer service scenarios like online chat support.
- **Contextual Understanding**: Translates not just words, but also phrases and sentences with cultural relevance.
- **Customizable for the Retail Sector**: Designed specifically for customer service interactions in retail.

## Model Performance
- **BLEU Score**: 51.4%
- **Precision**: 70.2%

### Example Translations:
- English: "Can I help you today?"
  - Igbo: "Enwene m ike inyere gị aka taa?"
  
- English: "We are sorry for the purchase error."
  - Igbo: "Anyị na-enye mgbaghara maka njehie."

## Prerequisites
- Python 3.7 or higher
- PyTorch
- Hugging Face Transformers library
- Tokenizers library
- CSV dataset containing English-Igbo translation pairs

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/mhixtadavid/English_to_Igbo_translation.git
   ```
   
2. **Navigate to the project directory**:
   ```bash
   cd English_to_Igbo_translation
   ```

3. **Create and activate a virtual environment**:
   ```bash
   python -m venv env
   source env/bin/activate  # For Windows, use `env\Scripts\activate`
   ```

4. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

5. **Download Pre-trained Model**: 
   Download the pre-trained translation model from Hugging Face and place it in the designated directory:
   ```bash
   python download_model.py
   ```

## Usage

1. **Preprocess Data**:
   Make sure your dataset of English-Igbo pairs is in CSV format. The file should be named `Igbo_corpus_2.csv` and placed in the `data/` directory.
   
2. **Run Training Script**:
   To train the model:
   ```bash
   python train.py --data_path data/Igbo_corpus_2.csv
   ```

3. **Run Translation**:
   To translate an English sentence to Igbo:
   ```bash
   python translate.py --text "Can I help you today?"
   ```
   Expected output:
   ```
   Enwene m ike inyere gị aka taa?
   ```

## Model Architecture
The system is built using a transformer model based on Hugging Face's architecture. It tokenizes English text, generates token sequences, and decodes them back into Igbo text. The model has been fine-tuned for accuracy using a curated dataset of 3200 translation pairs, with 80% used for training and 20% for testing.

## Dataset
The system uses a custom-built dataset, `Igbo_corpus_2.csv`, which contains 3200 English-Igbo sentence pairs. This dataset is split into 80% for training and 20% for testing. The dataset captures a variety of customer service interactions, specifically tailored to the retail sector.

## Challenges
- **Data Scarcity**: The Igbo language has fewer digital resources, making it difficult to source high-quality datasets.
- **Tonal Nature of Igbo**: Igbo is a tonal language, and capturing the subtleties of tone was a significant challenge.
- **Cultural Sensitivity**: Translating idioms and culturally significant phrases accurately required special attention to ensure the system resonated with Igbo speakers.

## Future Work
- **Expand Language Support**: Extend the system to other Nigerian languages such as Yoruba and Hausa.
- **Improve Real-Time Capabilities**: Further optimize the model for real-time translations in fast-paced customer service environments.
- **Data Augmentation**: Address data scarcity by exploring data augmentation techniques to improve model performance.

## Contributors
- **Your Name** – *Lead Developer*
- **Contributor Name** – *Research and Dataset Collection*
- **Contributor Name** – *Machine Learning Specialist*

## License
This project is licensed under the MIT License .
