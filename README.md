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
