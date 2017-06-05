# MLTK
A collection of self contained modules for machine learning.

## Dependencies
1. Tensorflow
2. Python 2.7

## Modules
### image_classifier
Utilizes the Inception engine to create a model for classifying images.

#### Setup
Create two different folders, one for training data and a second for testing purposes.  Within the training directory, divide `jpg` images into different categories via subdirectories.

```
- Animals
  - Cat
  - Dog
  - Mouse
```

Inception recommends at leaste 20 images per classification.

#### Learning
`cd /MTLK/modules/image_classifier`

```
python retrain.py   --bottleneck_dir=bottlenecks   --how_many_training_steps=500   --model_dir=inception   --summaries_dir=training_summaries/basic   --output_graph=retrained_graph.pb   --output_labels=retrained_labels.txt   --image_dir=Animals/
```

More information can be found here: https://codelabs.developers.google.com/codelabs/tensorflow-for-poets/?utm_campaign=chrome_series_machinelearning_063016&utm_source=gdev&utm_medium=yt-desc#4

#### Classify
`python label_image.py <path_to_image>`
