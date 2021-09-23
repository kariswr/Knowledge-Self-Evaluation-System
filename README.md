# Knowledge-Self-Evaluation-System

This project is code for **Knowledge Self-Evaluation System with Automatic Factoid Question Generator**. **Knowledge-Self-Evaluation-System** os a web based self-
evaluation system by generating factoid question from paragraph with 3 main component namely answer extractor, question generator, and answer grading. There is 2 different model implemented for answer extractor which is binary classification and a key phrase extraction model (BERT-Joint), sequence to sequence model is used for question generator. Lastly for answer grading a simple token based similarity is used.\

Here are the detail for each implemented model :
1. Binary Classification Answer Extractor : https://github.com/kariswr/Answer-Extraction
2. BERT-Joint Answer Extractor : https://github.com/kariswr/Multilingual-BERT-KPE
3. Question Generator and ANswer Grader : https://github.com/kariswr/Question-Generator-Api

For the web interface of the system can be accessed at : https://github.com/kariswr/ES-Front-End

## System's Architecture

![System's Architecture](https://github.com/kariswr/Knowledge-Self-Evaluation-System/blob/main/System's%20Architecture.jpg)

The system implemented intended to use on the web with a simple interface. System’s architecture is shown above with arrows represent access to the component being pointed
at. The answer extractor, question generator, answer grader component is accessible through API. Linguistic features such as POS tag and named entity will be obtained through Prosa.ai API.

## How to Use

In order to run this system, Prosa.ai API key is needed.

Steps to run the system are as follows :
1. Add the API key for Prosa.ai for binary classification answer extractor [at this](https://github.com/kariswr/Answer-Extraction/blob/main/src/preprocess/external_pos_ner.py#L6) and question generator [at this](https://github.com/kariswr/Question-Generator-Api/blob/master/src/preprocess/call_external_api.py#L6)
2. Run all API needed, only 1 API for answer extracted needed to be run. the default is BERT-Joint Answer Extractor since it has better performance.
3. Run the web interface.
4. Use the system through the interface. Happy Learning :)

