

# **Fine-Tuning LLaMA 3.1 for MCQ Generation**  

This Kaggle Notebook demonstrates the process of fine-tuning the **LLaMA 3.1** model for generating Multiple-Choice Questions (MCQs) from textual passages. It is part of a project to create a personalized learning platform that generates high-quality educational content and provides performance analysis for students.  

---

## **Notebook Highlights**  

- **Data Preprocessing**:  
  Extracts and cleans passages from NCERT textbooks (Classes 8–12) for use as the training dataset.  

- **Model Fine-Tuning**:  
  Leverages **LoRA** (Low-Rank Adaptation) and **4-bit quantization** for efficient fine-tuning of the LLaMA 3.1 model on limited computational resources.  

- **MCQ Generation**:  
  Uses structured prompts to generate contextually aligned MCQs, with varying difficulty levels based on **Bloom's Taxonomy**.  

- **Evaluation**:  
  Includes methods for evaluating the model's outputs using BLEU scores and qualitative assessment.  

---

## **How to Use**  

### **Running the Notebook**  

1. **Kaggle Environment**:  
   Open the notebook on Kaggle and ensure a GPU runtime is enabled.  

2. **Dataset Upload**:  
   - The dataset used for training must include cleaned passages and corresponding MCQs in CSV format.  
   - Example dataset format:  
     | Passage         | MCQs                 | Answer Key | Difficulty Level |  
     |-----------------|----------------------|------------|------------------|  
     | Sample passage  | Question options... | Answer...  | Easy             |  

3. **Execute Cells**:  
   Run each cell sequentially to:  
   - Prepare the dataset.  
   - Fine-tune the model.  
   - Generate MCQs for evaluation.  

4. **Output**:  
   Generated MCQs will be saved or displayed as output in the notebook.  

---

## **Requirements**  

The notebook is pre-configured for Kaggle, but the following libraries are essential:  

- **Transformers**  
- **PEFT**  
- **BitsAndBytes**  
- **Datasets**  

Install any missing libraries using:  
```bash
!pip install transformers peft bitsandbytes datasets
```  

---

## **Key Steps**  

1. **Data Preprocessing**:  
   - Text passages were extracted from NCERT textbooks and cleaned to remove irrelevant details.  

2. **Model Setup**:  
   - LLaMA 3.1 was fine-tuned using **LoRA** with 4-bit quantization to optimize GPU memory usage.  

3. **Training**:  
   - The model was trained on structured prompts to generate high-quality MCQs with answer keys.  

4. **Evaluation**:  
   - Model outputs were evaluated to ensure accuracy and contextual relevance.  

---

## **Results**  

- The fine-tuned model outperformed baseline configurations, demonstrating high accuracy in generating MCQs across multiple difficulty levels.  
- Sample outputs and metrics are displayed in the notebook's final cells.  

---

## **Acknowledgments**  

- **NCERT** for providing open-access textbooks as a source for the dataset.  
- Hugging Face for pre-trained models and tools.  
- Kaggle for hosting the computational environment.  

---

## **License**  

This notebook is licensed under the MIT License. Feel free to use and adapt the code for educational and research purposes.  

---
