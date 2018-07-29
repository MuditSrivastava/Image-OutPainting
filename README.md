# Keras implementation of Image OutPainting

This is an implementation of [Painting Outside the Box: Image Outpainting](https://cs230.stanford.edu/projects_spring_2018/posters/8265861.pdf) paper from Standford University. 
Some changes have been made to work with 256*256:
  - Added Identity loss i.e from generated image to the original image
  - Removed patches from training data. (training pipeline)
  - Replaced masking with cropping. (training pipeline)
  - Added convolution layers.

## Results
The model was train with [beach data](http://cvcl.mit.edu/scenedatabase/coast.zip)  for 200 epochs.

## Tested with
  - python 3.5
  - keras==2.1.5
  - keras-contrib==2.0.8
  - tensorflow==1.5.0
  - opencv-python==3.4.0.12
  - CUDA Version 9.0.176

## Get Started
1. Prepare Data:
  ```sh
  # Downloads the beach data and converts to numpy batch data
  # saves the Numpy batch data to 'data/prepared_data/'
  python3 prepare_data.py
  ```
2. Build Model
  * To build Model from scratch you can directly run 'outpaint.ipynb'
  <br/>OR<br/>
  * You can [Download](https://drive.google.com/file/d/1548iAtsNf3wLSc1i5zYy-HX8_TW95wi_/view?usp=sharing) my trained model and move it to 'checkpoint/' and run it.

## References
* [Painting Outside the Box: Image Outpainting](https://cs230.stanford.edu/projects_spring_2018/posters/8265861.pdf)