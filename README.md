# Appoach3-StyleTransferFromVideo

In this project, we are aiming for  identifing which aspects of the character animation affect the user’s perception and interaction with the character (agent). Therefore we applied  a style transfer approach taken from Kfir Aberman that tune the style of 3D animations directly from videos.An ability which enables one to extend the set of style examples far beyond motions captured by MoCap systems.

## Attribution

The core code used in this project was created by Kfir Aberman et al. [Link-to-original-code-repo](https://github.com/DeepMotionEditing/deep-motion-editing). Their paper can be found 
[Here](https://deepmotionediting.github.io/papers/Motion_Style_Transfer-camera-ready.pdf).

## Modifications and Use Case

I have adapted the original code to suit the requirements of my use case. The modifications include Retraining the model on our proper Dataset and adding pose detection of TedTalks videos. This adaptation allows the code to effectively address the unique needs of targeting style linked to the traits of personnality (ex: Neurotic, emotionally stable..).

## How to Use
1. Dataset:
Put VirtUS dataset in style_transfer/data , this Datset should retargeted to CMU mocap structure , then prepocess it like this :

```python
cd style_transfer/data_proc
sh gen_dataset.sh
```  
2. Test:
To receive the demo examples, simply run

```python
sh style_transfer/demo.sh
```
The results will be saved in style_transfer/demo_results

3. retrain:
```python
python style_transfer/train.py
```

5. In case you want to add extra videos, you need to extract 2D joint positions from the video using [OpenPose](https://github.com/CMU-Perceptual-Computing-Lab/openpose) , then use the resulting JSON files
## Acknowledgments

I would like to express my gratitude to Kfir Aberman et al. for creating the initial codebase. Their contribution laid the groundwork for the enhancements made in this project.



## Contact

If you have any questions, suggestions, or feedback, feel free to reach out to me at ghammaz.ali1@gmail.com .
