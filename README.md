# BengaliAI-Speech-Recognition-31st-place-solution
Team AudioAlchemists secured the 31st position in the research competition "Bengali.AI Speech Recognition Challenge" hosted on kaggle. This repositpry contains the training and inference codes of our solution.

The inference notebook can also be found [here](https://www.kaggle.com/code/mbmmurad/31st-place-inference-notebook) in Kaggle.
A detailed description of our solution can be found [here](https://www.kaggle.com/competitions/bengaliai-speech/discussion/448030)

Please follow the following steps to reproduce our work.

## Set up
```
pip install -r requirements.txt
```

## Prepare Data
We used three datasets here.
1. **Competition dataset** : The hosts of the competition provided about 1200 hours of recordings of Bengali speech. The dataset can be downloaded from [here](https://www.kaggle.com/competitions/bengaliai-speech/data)
2. **Openslr37**: High-quality TTS data for Bengali languages. Can be downloaded from [here](https://www.openslr.org/37/)
3. **Openslr53**: Bengali ASR training data set containing ~196K utterances. Can be found [here](https://www.openslr.org/53/)

After downloading the datasets, please convert the audios to mp3 and place all the audios in the ```full_data/train_mp3s``` folder and place the metadata files(.csv,.tsv) in the ```full_data``` folder.

## Training
### Wav2vec2 fine-tuning
We finetuned ```ai4bharat/indicwav2vec_v1_bengali``` model on our dataset. The details about the pre-trained model can be found [here](https://github.com/AI4Bharat/IndicWav2Vec).
To finetune this model please follow the ```31st_Place_Training_Notebook.ipynb``` notebook. ALl the necessary steps are described there.
### Language model
We trained a 5-gram language model on several datasets. Please follow the ```fork-of-creating-n-gram-language-model-for-wav2vec.ipynb``` notebook. This training notebook can also be used from [Kaggle](https://www.kaggle.com/code/mbmmurad/fork-of-creating-n-gram-language-model-for-wav2vec/notebook)

## Inference
For inference please follow the ```31st-place-inference-notebook.ipynb``` notebook. It can also be accessed from [Kaggle](https://www.kaggle.com/code/mbmmurad/31st-place-inference-notebook)

