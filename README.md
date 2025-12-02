# 🧠 SQLearn — A Fine-Tuned LLM for Learning SQL

## 📌 Project Overview
SQLearn is a lightweight, instruction-tuned chatbot designed to teach SQL concepts, write SQL queries, debug SQL code, and convert natural language into SQL.  
This project is created to demonstrate how a useful domain-specific LLM can be built **without a GPU**, using **open-source models** and **low-compute fine-tuning techniques** such as **LoRA/QLoRA**.

## 🎯 Objective
The goal of SQLearn is to help beginners and intermediate learners understand SQL step-by-step through:
- Clear explanations of SQL concepts  
- Example-driven learning  
- Query generation  
- Natural-language-to-SQL translation  
- SQL debugging  
- Real-world database problem solving  

SQLearn serves as a practical example of how anyone with limited hardware can fine-tune a small LLM for a focused, educational use case.

## 💡 Why This Project?
Most LLM fine-tuning tutorials assume access to GPUs and large datasets.  
SQLearn takes the opposite approach:
- Uses **small open-source models** (1B–3B parameters)
- Trains on a **small curated dataset** (50–200 examples)
- Runs entirely on **CPU**
- Produces a **high-quality domain expert bot**

This makes it ideal for students, educators, and developers wanting to learn fine-tuning without expensive hardware.

## 🏗️ Key Features
- **Instruction-tuned SQL assistant**
- **Domain-focused dataset (manually curated + synthetic examples)**
- **LoRA/QLoRA fine-tuning on CPU**
- **Simple inference API (Flask/Streamlit)**
- **Deployable as a web chat, CLI chat, or WhatsApp bot**

## 📁 Project Structure

```
SQLearn/
│
├── data/
│   ├── sqlearn_dataset.json         # Final instruction-response dataset
│   └── raw/                         # Optional raw text or CSV files before formatting
│
├── notebooks/
│   └── Dataset_Creation.ipynb       # Jupyter notebook for dataset generation and testing
│
├── training/
│   ├── finetune_lora.py             # QLoRA/LoRA fine-tuning script
│   └── config.yaml                  # Training configurations (model name, lr, epochs, etc.)
│
├── model/
│   ├── base_model/                  # Pretrained small open-source model (downloaded)
│   └── sqlearn_lora_model/          # Output of fine-tuned LoRA model
│
├── app/
│   ├── api/
│   │   └── main.py                  # Flask API to serve the fine-tuned model
│   │
│   └── ui/
│       └── app.py                   # Streamlit or Gradio front-end for chatting with SQLearn
│
├── utils/
│   ├── data_utils.py                # Cleaning, formatting, and dataset generation helpers
│   └── model_utils.py               # Model loading, inference helpers
│
├── tests/
│   ├── test_dataset.py              # Validate dataset formatting
│   └── test_inference.py            # Validate responses from model
│
├── requirements.txt                 # Python dependencies
├── README.md                        # Main project documentation
└── LICENSE                          # License (MIT recommended)

```
## 📚 Skills Covered
This project helps you learn:
- LLM fine-tuning with LoRA/QLoRA
- Building custom datasets for domain experts
- Model loading and inference using Transformers + PEFT
- Deploying an LLM as a web service
- Practical SQL problem framing

## 🚀 Use Cases
- SQL tutoring for beginners  
- Data science and DBMS training  
- Interview preparation  
- Teaching SQL in classrooms  
- Custom database assistants for organizations  

---

**Next Step:**  
You may continue by generating the dataset, setting up the fine-tuning script, or building the chatbot interface.
