# Stable Audio Open Finetune Proof of Concept

The notebook that actually runs the training is ```tune.ipynb```. Below is a brief description of what each file contains.

## Files
- ```dataset.json``` - This defines the data being used, points it to a path as well as to a python script that tells the model how to use the data in training.
  
- ```dataset.py``` - This file is the script that defines what information from the dataset is being fed to the model and how, this is pointed to by the aforementioned ```dataset.json```
  
- ```di dataset.ipynb``` - This is the notebook used for gathering the prototype data (probably not useful moving forward but keeping for reference). It also pulls the ```model_config.json``` as well as the stable audio open checkpoint from the official huggingface.
  
- ```model_config.json``` - This is the model config pulled from the stable audio huggingface with some modifications. The modified parameters were the following:
  - ```sample_size```
  - And then just the demo configurations:
    - ```demo_every```
    - ```num_demos```
    - the demo prompts
    - ```demo_cfg_scales```
      
- ```tune.ipynb``` is ****the notebook used for training****, this is also where the model is unwrapped. This is the meat and potatoes and where all the other files are pointed to.

All of this is based off of this [very helpful youtube video](https://www.youtube.com/watch?v=ex4OBD_lrds&t=2415s&themeRefresh=1)
