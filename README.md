# Image-Classification-using-TPU
Python notebooks for converting Image Dataset folder into TFRecord files and training Image Classification model in TPU

These notebooks are created to simplify the image classification process and use the Google's TPU accelerator. 

The Tensor Processing Unit (TPU) hardware accelerators are very fast. The challenge is often to feed them data fast enough to keep them busy. We are going to batch the data in a smaller number of files and use the power of tf.data.Dataset to read from multiple files in parallel.

Create TFRecords for Image Classification notebook can be used to create tfrecord files from a Image Dataset directory. Images should be divided into different class folders in Image Dataset directory  Ex /img_dir/cat, /img_dir/dog. This notebook supports train,test and validation directories or splitting a single directory into train,test and validation sets. Running this notebook will output TFRecord files for train,test and validation sets.

These TFRecord files should be stored in Google Storage bucket for TPU usage. You can get GS bucket path of Kaggle public datasets. So you can create a public dataset by uploading these TFRecord files.

Image classificatio with TFRecord files notebook can be used to access the data stored in TFRecord files usinf tf.data.Dataset and train the model in TPU. It also supports CPU and GPU. You can change the keras model definition , but make sure the input size is correct.

These notebooks are available in the Kaggle: 
https://www.kaggle.com/karthikeyanvijayan/create-tfrecord-files-for-image-classification,
https://www.kaggle.com/karthikeyanvijayan/image-classification-using-tfrecord
