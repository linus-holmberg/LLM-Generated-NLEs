This is a guide to replicate the NLEs used in the User Study. 

Steps:
    1. Run "1_SVC_text_data_and_preds.ipynb" as is. To train the SVM and generate a CSV-file with LIME explanations for the instances inclueded in the user study. 
    2. Run "2_CSV_to_Prompt.ipynb" as is. This will generate a CSV-file with prompts. 
    3. Open "params_LLM.json" and enter an OpenAI key for the API call. Moreover, set "include" to 'yes' if you want to generate explanations with LIME rationales, or 'no' if you want to generate explanations without LIME rationales. 
    4. Run "3_Generate_NLEs.ipynb". You have now generated natural language explanations. 
    -- If you want to generate explanations both with and without rationales, simply repeat step 3-4 but change "include" in "params_LLM.json". Also, remember to feed the new CSV file to "3_Generate_NLE_faithfulness.ipynb"

    5. Run "4_Faithfulness_Assessment.ipynb". This will procude the F1, recall, accuracy, and precision as in the thesis. 
    -- Moreover, this will also generate a CSV-file containing all instances and the information needed for the qualitative assessment. 

