# Deep-Learning-Based-Facial-Expression-Recognition-and-Face-Recognition-Model

Masters Thesis

Deep Learning Based Facial Expression Recognition and Face Recognition Model
This repository contains the code that I used to train the models mentioned in my Masters thesis. When processing data, I often omitted writing a script and worked in the python shell directly, for example while saving the AffectNet images into NumPy arrays.

I trained my models using the train.py script which has a command-line interface for handling training parameters such as the number of epochs or the batch size. The models BASE, COV and STN-COV can be found in the file keras_models.py. They are called DenseNet121, DenseNet121CovDropout and STNDenseNet121CovDropout respectively. Other models that I tried during my thesis can be found in the directories residual_attention_network, keras_vggface or keras_applications or in one of the following files: bregnet.py, ensemble.py, holonet.py, lightcnn.py, model.py, ran.py, resnet50plus.py, squeezenet.py.

The training batches that all contain the same amount of images from each category are created by the TrainDataGenerator and the ValDataGenerator which can be found in the file generator.py. They have a lot of parameters because I experimented a lot, but in the end I often used the standard configuration and just specified the batch_size and maybe one or two other parameters. Please note that you have to set augment=False in the ValDataGenerator if you want to have meaningful comparisons of the validation accuracy of different models.
