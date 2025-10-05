Geez Chatbot Project  NB: any one can see its contents by downloading the folder and open using visual studio or google colab.
====================

This repository contains the implementation of an intelligent Geez chatbot designed to understand and respond to user inputs in the Geez script, an ancient Ethiopic language. The project aims to support low-resource language processing using the mT5 transformer model, enhancing conversational AI for underrepresented languages like Geez, Tigrigna, and Amharic.

🌍 Project Purpose
------------------
The chatbot was developed as part of an academic and research-based NLP project to:

• Preserve and support the Geez language using modern AI.  
• Explore low-resource language modeling.  
• Pretrain and fine-tune a transformer-based model using custom datasets.  

📁 Project Structure
--------------------
Geez_chat_bot_project/
│
├── Geez_chat_bot.ipynb            # Main Jupyter notebook for training and evaluation  
├── datasets/
│   ├── kufale.json                # Geez-English translation dataset  
│   ├── ግዕዝ_ጥያቄ_ወአውስኦ.csv          # Geez Question-Answer dataset  
│   ├── processed_translations.csv # Preprocessed translation pairs  
│   ├── processed_qa.csv           # Preprocessed QA pairs  
│   └── processed_geez_tigrigna.csv# Geez-Tigrigna dataset  
└── README.md                      # Project documentation  

🔧 Technologies Used
--------------------
• Python 3.10+  
• HuggingFace Transformers  
• HuggingFace Datasets  
• PyTorch  
• Google Colab / Jupyter Notebook  
• BLEU & ROUGE for evaluation  

🧠 Model Overview
-----------------
• Base Model: google/mt5-small  
• Pretraining: Custom datasets (translations + QA) about 6000 datasets combination 
• Fine-Tuning: Focused on QA task using Geez-specific question-answer pairs (finetune on 500 geez to geez conversational datasets) 

📊 Datasets
-----------
• kufale.json – Geez ↔ English sentence pairs (~3000 lines)  
• ግዕዝ_ጥያቄ_ወአውስኦ.csv – Geez QA pairs (~400 rows)  
• processed_geez_tigrigna.csv – Geez ↔ Tigrigna samples for multilingual enhancement  

📈 Evaluation Metrics
---------------------
• BLEU Score – Evaluates translation fluency  
• ROUGE Score – Evaluates overlap with reference answers  

✅ Key Features
---------------
• Multi-language support: Geez, Tigrigna, English  
• Trained on low-resource languages  
• Modular and extensible code  
• Tokenizer handling for Geez script  
• Includes preprocessing, training, and evaluation pipeline  

🚀 How to Run
-------------
1. Clone the repository:
    git clone https://github.com/selemun-dev/Geez_chatbot.git  
    cd Geez_chatbot

2. Launch the google colab or Jupyter Notebook:
    jupyter notebook Geez_chatbot.ipynb

3. Train the model or test on custom input.

**Note:** Training is optimized for Google Colab using early stopping and batch tuning.

📌 Future Work
--------------
• Build a dedicated tokenizer for Geez script  
• Expand the dataset to include real conversations   
• Train larger mT5 variants (base, large) if resources permit  

📜 License
----------
This project is licensed under the MIT License.  
You are free to use, copy, modify, and distribute this software for any purpose, with attribution.
