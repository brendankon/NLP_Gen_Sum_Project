# Decoding Strategies for Code Conciseness and Efficiency in Transformer-Generated Programs

Below is a description of the main code elements of the project:

**CodeBLEU** - Implementation of the CodeBLEU evaluation metric as described in Ren et al., 2020. Implementation provided by Microsoft: https://github.com/microsoft/CodeXGLUE/tree/main/Code-Code/code-to-code-trans/evaluator/CodeBLEU

**neurologic_astar** - Implementation of the NeuroLogic A* decoding algorithm as described in Lu et al., 2021, with modifications made for the use of line and loop penalization terms as described in our paper. Base implementation provided by https://github.com/GXimingLu/a_star_neurologic

**test_one_solution.py, testing_util.py, reindent.py** - Helper functions for automatically scoring model generated programming solutions against APPS dataset test cases. Implementation provided by https://github.com/hendrycks/apps

**decoding_analysis.ipynb** - Main jupyter notebook containing custom written code for:
  **1.)** Loading in training and testing data from APPS dataset and filtering based on problem type and model constraints
  **2.)** Finetuning a pretrained CodeT5 transformer model on APPs training data
  **3.)** Defining custom beam search function with line and loop penalization terms
  **4.)** Generating solutions from custom CodeT5 and pretrained GPT-2 models over APPS test data using various decoding strategies
  **5.)** Generating summary statistics about model generations such as test case performance, new-line and loop operations generated, CodeBLEU evaluations based on human generated solutions, and runtime/compile errors
  
 ## Models
 The two models utilized for experimentation are CodeT5 and GPT-2. Locations to both of the saved models can be found below:
 
 **CodeT5** - https://drive.google.com/drive/folders/1ljowu88BbfhrIymmUDSY_u52w6TnWiZv?usp=sharing
 **GPT-2** - https://drive.google.com/file/d/1XW1Od9L-5l9zXl1HUCyER5pS9zQTbIvU/view?usp=sharing
