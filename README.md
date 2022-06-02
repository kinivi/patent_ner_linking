# Named entitity recognition (NER) and Entity linking (EL) on the dataset of Patents

The main goals of this project are:
- Train NER model with dataset of Patents in the specific domain
- Fine-tune with prodidy 
- Implement EL with Hearst patterns
- Validate linking results with several methods, inluding Wikidata

## Structure
- [project.ipynb](./project.ipynb) - main notebook
- [G06K.txt.gz](./G06K.txt.gz) - archive with patent texts
- [patterns.json](./patterns.json) - Hearst patterns configuration for SpaCy

## Setup
1) Install dependencies from [requirements.txt](./requirements.txt)
2) Unpack data:  
`tar -xvf G06K.txt.gz`
3) Open [project.ipynb](./project.ipynb) and run first cell to chek that all imports works propperly
## Notebook structure
### Data processing
### Training NER model
### Hearst patterns for EL
### Automatic validation of EL results
---

## 🫡 Thanks 
