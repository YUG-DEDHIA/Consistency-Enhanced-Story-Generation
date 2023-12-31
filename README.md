# Consistency-Enhanced-Story-Generation
## Team-12 
<div dir ='rtl'>
Rishabh Srivastava(2020101047)
</div dir='ltr'>
<div dir ='rtl'>
Yug Dedhia(2020115004)
</div dir='ltr'>
<div dir ='rtl'>
Rishabh Jain(2020111003)  
</div dir='ltr'>


# Writing Prompts Data Processing

The code combines source and target data, extracts keywords, and generates abstracts for the stories. It is designed to assist in data preprocessing for natural language processing tasks.

## Getting Started

### Prerequisites

Before running the code, ensure you have the following libraries installed:

- `numpy`
- `pandas`
- `csv`
- `rake_nltk`
- `sumy`

You can install these libraries using `pip`:

```bash
pip install numpy pandas csvkit rake-nltk sumy
```

### Usage

1. **Combining Source and Target Data**

   - Modify the `DIR` and `TARGET_DIR` variables in the code to specify the directory paths for your data files.
   - Run the code to combine source and target data for training, testing, and validation datasets.
   - CSV files named `combined_traindata.csv`, `combined_testdata.csv`, and `combined_valdata.csv` will be created.

2. **Extracting Keywords and Generating Abstracts**

   - The code uses the RAKE algorithm for keyword extraction and the LexRankSummarizer for abstract generation.
   - Ensure you have the CSV files (`combined_traindata.csv`, etc.) in the same directory as the code.
   - Run the code to process the data and generate (prompt, outline, story) triplets.
   - A new CSV file named `new_traindata.csv` will be created, containing the processed data.
    
3. **To Run single stage story generation**
   - Update src/config.yml accordingly
   - Run *python single_stage.py* to train and validate the model.
   
4. **To Run double stage story generation**
   - Update src/config.yml accordingly
   - Run *python double_stage.py* to train and validate the model.
   
5. **To include discourse coherency story generation**
   - Update src/config.yml accordingly
   - Run *python discourse.py* to train and validate the model.
   
