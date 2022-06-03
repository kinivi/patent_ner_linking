# Named entitity recognition (NER) and Entity linking (EL) on the dataset of Patents

The main goals of this project are:
- Train NER model with dataset of Patents in the specific domain
- Fine-tune with prodidy 
- Implement EL with Hearst patterns
- Validate linking results with several methods, inluding Wikidata

## Structure
- [project.ipynb](./project.ipynb) - main notebook
- [G06K.txt.gz](./G06K.txt.gz) - archive with patent texts
- [configs/base_config.cfg](./configs/base_config.cfg) - Base config to train NER SpaCy pipeline
- [hearst_patterns/patterns.json](./hearst_patterns/patterns.json) - Hearst patterns configuration for SpaCy
- [extracted_patterns](./extracted_patterns) - Extracted patterns (EL) from G06K texts

## Setup
1) Install dependencies from [requirements.txt](./requirements.txt)
2) Unpack data:  
`tar -xvf G06K.txt.gz`
3) Open [project.ipynb](./project.ipynb) and run first cell to chek that all imports works propperly
## Notebook structure
Here is a brief overview of the [project.ipynb](./project.ipynb) parts.
### Data processing
<p align="left">
<img width="288" alt="Screenshot 2022-06-03 at 11 14 57" src="https://user-images.githubusercontent.com/13486777/171825899-a2840718-a1b3-4b7b-817a-6655eca3e334.png">
</p> 

In this section patent text read and prcessed to extract potential Named entities using curated list of terms [manyterms.lower.txt](./manyterms.lower.txt)



### Training NER model
<p align="left">
<img width="288" alt="Screenshot 2022-06-03 at 11 21 47" src="https://user-images.githubusercontent.com/13486777/171827126-9f090a9b-88c1-4f07-a77a-abd2ded36a3c.png">
</p> 

Next, we are training the model on the created dataset.  
Additionaly, if you have access to the Prodiy, you can apply Active Learning to tune the model. 

### Hearst patterns for EL
<p align="left">
<img height="100" alt="Screenshot 2022-06-03 at 11 33 11" src="https://user-images.githubusercontent.com/13486777/171829037-4c3fbd3c-a4be-4e0a-b6f9-2a866b64bc30.png">
</p> 
Thise section is dedicated to extracting potential Entity linking (like hypernyms) using Hearst Patterns.

### Automatic validation of EL results
<p align="left">
<img height="100" alt="Screenshot 2022-06-03 at 11 34 55" src="https://user-images.githubusercontent.com/13486777/171829378-7bfd461d-d702-414e-a29d-f04bafd4e22e.png">
</p> 
Afte extraction, we validate results automatically, using Wiki API, WordNet or SpaCy embeddings. Here is an example of validation table after processing:

![hq2SyK1SEvKTISY0DtddgY_mF9j966vIPi8Fhm26nJq-xPNc_NH0xPhap97ZAruJOHaEjqbf7a2-kKwSZnw6JeRFH9dwk2w06Dd9OjTOq3EmgRbpmFAYIIuyTphYtAeqcYa70NWnW_9ZwK4cGmEv0A](https://user-images.githubusercontent.com/13486777/171829683-9071bfea-6aea-474d-bb08-59559703d70b.png)

<!-- ---

## 🫡 Thanks  -->
