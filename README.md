# Speech Command Model
![Python 3.6](https://img.shields.io/badge/Python-3.6-brightgreen.svg) ![kapre 3.6](https://img.shields.io/badge/Kapre-0.1.7-blue.svg) ![Tensorflow-gpu](https://img.shields.io/badge/Library-Scikit_Learn-orange.svg) ![Soundfile-gpu](https://img.shields.io/badge/Library-Soundfile-yellow.svg) ![tf](https://img.shields.io/badge/Tensorflow-2.2.0-red.svg)

![Speech voice Recognition Header](https://github.com/ayushkesh/speech/blob/master/a.jpg)

1. [ Overview ](#overview)
2. [ Data Creation ](#Data Creation)
3. [ Description ](#Description)
4. [ Installation and Run](#Installation and Run)


<a name="overview"></a>
### Overview
From smart lights that turn on or off on your command, Google Home Assistant that can place space trivia 
with you and make financial transactions when requested, Alexa that can place your grocery order and call you 
a cab on your behalf, to automobiles, refrigerators, and washing machines that follow your voice commands; speech recognition 
is the component of the system that makes it all possible. in similar way Speech voice recognition model is based on
concepts of Convolution, LSTM and Attention and recognise pretrained voice with accuracy of 97%.

#### Data Creation
1. Set 16KHz as sampling rate
2. Record 80 utterances of each command.
3. Save samples of each command in different folders
- Dataset/forward
- Dataset/back
- Dataset/left
- Dataset/right
- Dataset/stop



### Description
1. Using Convolutional layers ahead of LSTM is
shown to improve performance in several research papers.
2. BatchNormalization layers are added to improve convergence rate.
3. Using Bidirectional LSTM is optimal when
complete input is available. But this increases
the runtime two-fold.
4. Final output sequence of LSTM layer is used to
calculate importance of units in LSTM using a
FC layer.
5. Then take the dot product of unit importance
and output sequences of LSTM to get Attention scores of each time step.
6. Take the dot product of Attention scores and
the output sequences of LSTM to get attention
vector.
7. Add an additional FC Layer and then to output
Layer with SoftMax Activation.
- The model is successfully built and has achieved the highest accuracy of __97.02%__

### Installation and Run
The Code is written using  __Google Colab__
1. Open ColabNotebook.ipynb and change Runtime to GPU
2.  Upload Data/Ayush_17 to Colab.
4.  Change data_dir in all cells to point to Ayush_17
5.  Run the cells in the same order in Notebook.
