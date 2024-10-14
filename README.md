# A CNN fast training and testing tool

This implamentation is built on top of Keras and Tensorflow to fast train any Keras Model and test them on any dataset.

Dataset format for Folder use:
```
    - dataset:
        - class 1
        - class 2
        - class 3
        - ...
        - class n
```

For loading the dataset from Tensorflow API you need to know the 'title' of the dataset. You can find it at the following link, under the Image section:

<a href="https://www.tensorflow.org/datasets/catalog/overview"> https://www.tensorflow.org/datasets/catalog/overview </a>

How to use for Folder format stored on a drive (local or cloud):
```
    0. Run "Balance Dataset from folder" block (optional, only if needed)

    1. Run "Dataset from folder" block
    2. Run "Training" block
    3. Run Keras Model block (in this case "FFTConv2D Tensorflow Keras" and "VFFT-CNN" block, but it can be replaced with your own Keras Model)
    4. Run "Benchmark dataset load" block (replace "dataset_path" with your own path and adjust the output dataset parameters like with, batch_size, augment, etc.)
    5. Run "Benchmark" block to train and test the model, an excel file will be saved out of the dataset folder with the training and testing results like training time, accuracies, FLOPS etc. (replace the Keras Model with your own model and adjust the epochs). Also a .keras and .tflite files will be saved with the best model.

    6. Run "Confusion Matrix" (optional, replace Keras Model path)
    7. Run "CNN Filters plot" (optional, replace Keras Model path)
```

<a href="https://github.com/cococialin/vfft-cnn"> VFFT-CNN </a> is first presented in my Phd Thesis titled: NATURAL INSPIRATION METHODS FOR ENHANCEMENT OF ENVIRONMENTAL INFORMATION RECOGNITION IN MOBILE COMPUTING PLATFORMS

If you find it usefull please cite.
