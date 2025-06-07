# 🧠 textify-VQA

**textify-VQA** is a Vision-Question-Answering (VQA) project focused on answering product-related questions using both visual and textual information from product images. The project leverages an Amazon product dataset and introduces a custom model that significantly improves performance on structured data queries like nutrition facts.

---

## 📌 Project Objective

The goal of `textify-VQA` is to accurately answer questions about product attributes—especially those embedded in tables—by integrating:

- Visual content of product images
- OCR-based textual features
- Pretrained and fine-tuned VQA models
- A custom hybrid architecture for deeper visual-textual understanding

---

## 🧰 Key Features

- ✅ Pretrained **BLIP** model for answering general visual questions  
- ✅ Fine-tuned **BLIP** model adapted to Amazon product QA data  
- ✅ Custom VQA architecture combining:
  - OCR text features (text, bounding boxes, orientation)
  - Visual embeddings
  - Question embeddings  
- ✅ Strong performance on table-related questions (e.g., nutritional facts, calorie content)


---

## 📦 Dataset

The dataset is an **Amazon product VQA dataset**, consisting of:

- Product images
- User-generated questions and answers
- A mix of visual and text-based queries, especially from packaging and tables

---

## 🔍 Methodology

### 1. Raw BLIP Evaluation
Run zero-shot inference using the base BLIP model to answer general visual queries (e.g., product color, shape).

### 2. Fine-Tuned BLIP
Adapt BLIP to domain-specific questions by fine-tuning it on the Amazon dataset to improve accuracy.

### 3. Custom OCR-Based Model
Introduce a novel architecture that integrates:
- OCR features (extracted text, position, angle)
- BLIP visual features
- Question embeddings from a language model
- Multimodal fusion for enhanced understanding of structured data in images

---
## 📊 Results Summary

| Model            | Visual Q Accuracy | Table Q Accuracy   |
|------------------|-------------------|--------------------|
| Raw BLIP         | ✅ Good           | ❌ Poor            |
| Fine-tuned BLIP  | ✅ Better         | ⚠️ Moderate        |
| Custom Model     | ✅ Good           | ✅ Excellent        |

---

## 🚀 Getting Started

### Install dependencies

```bash
pip install -r requirements.txt
```
### Prepare the dataset
```bash
# Download images and convert metadata
Run prepare_dataset.ipynb
```
### Run raw BLIP inference
```bash
Run test_raw_blip.ipynb
```
### Fine-tune BLIP
```bash
Run finetune_blip.ipynb
```
### Train and evaluate custom model
```bash
Run custom_model.ipynb
```
---

## 📌 Future Work
- Improve OCR accuracy with larger models (e.g., Donut, LayoutLMv3)

- Unified transformer architecture for joint learning

- Deployment as an API or web app for live inference

- Multilingual support

## 🤝 Acknowledgements
- BLIP (Salesforce)

- HuggingFace Transformers

- Amazon VQA Dataset

## 📃 License
MIT License

