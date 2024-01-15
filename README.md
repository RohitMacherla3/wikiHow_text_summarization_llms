# wikiHow_text_summarization_llms
Deployed Models:
1. LoRA Fine Tuned Model - https://huggingface.co/rohitmacherla3/wikihow_t5small_LoRA_fine_tuned
2. Simple Fine Tuned Model - https://huggingface.co/Prashanth-1998/wikihow_t5small_model


### Team:
1. Prashanth Aripirala
2. Rohit Macherla
3. Vishal Reddy Mekala

### Task - Text Summarization
The project aims to utilize pre-trained Large Language Models (LLMs) for text summarization through diverse fine-tuning techniques. Comparative analysis with baseline RNN/LSTM language models is undertaken, utilizing established metrics such as Rouge score and BLEU.

### Dataset:  
A large-scale text summarization dataset (600 MB) was procured from the WikiHow knowledge database. 
Each article in the dataset has a title, a summary which is the concatenation of the headlines of all the paragraphs to serve as the reference summary, and the text which is the concatenation of all the text except the headlines used in the summary variable.

### Dataset Specifications:
The selected wikiHow dataset encompasses approximately 215k data points
For preliminary testing, 10% of the data was utilized for training and 5% for testing. Future scaling considerations will be contingent upon the outcomes of these initial tests.

<img width="468" alt="image" src="https://github.com/RohitMacherla3/wikiHow_text_summarization_llms/assets/89356811/ce4dccbb-7730-48f0-ade0-f4cd68f79d11">


### Data Preprocessing:
Thorough preprocessing of the WikiHow dataset was conducted to ensure a robust foundation for subsequent model training. Missing values were removed to maintain data integrity. The Natural Language Toolkit (NLTK) library was employed for stopword removal, enhancing the textual content's quality. Dedicated functions, namely text_cleaner, and summary_cleaner, were used to process the main text and headline summaries, preparing the data for training.

Train-Test split: The training dataset consists of 19,899 data points, resulting in a 75-25 split with the test dataset, which includes 4,976 data points.

Tokenization/Embeddings: Conversion of input text and target summaries into vector spaces suitable for model input was performed.

Padding: Ensured uniform length of input sequences for efficient batch processing through end-based padding, accommodating the largest embedding size.

### Models and Fine-Tuning Techniques Used
- Baseline
  1. seq2seq - LSTM
  2. seq2seq - Transformer
- Pre-trained
  1. BART-Base
  2. T5-Small
- Fine-Tuning Techniques
  1. Simple Fine-tuning
  2. LoRA Fine-tuning
 
### Evaluation Metrics
ROUGE and BLEU scores are computed for each model for evaluation

<img width="564" alt="image" src="https://github.com/RohitMacherla3/wikiHow_text_summarization_llms/assets/89356811/ebf09f94-006d-4b5b-bda9-39a8d549bd33">




