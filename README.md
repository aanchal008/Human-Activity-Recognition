# Human-Activity-Recognition

Human Activity Recognition can be immensely used in
healthcare applications for automatic and intelligent daily
activity monitoring. When a person performs various activities in day-to-day life, his smartphone collects the sensory
data sequence and extracts high-efficiency features from
original data. Thus with the help of three axial time series
data collected by accelerometer and gyroscope, a user’s
physical behaviour can be depicted. The project aims to
train a deep neural network to recognize one of the six given
physical activities, namely ’Walking’, ’Jogging’, ’Upstairs’,
’Downstairs’, ’Sitting’, and ’Standing’.

----------------------------------------------------------------------------------------------------------------------------------------------------------

# Model Details

During training, the records are fed into the neural network
after reshaping. Each person has multiple two-dimensional
records, which holds 80-time slices for each of the accelerometer readings. one record is associated with only
one label. The labels are one-hot encoded. Categorical
cross-entropy is used to calculate the loss. While compiling
the model, adam optimizer is used with default learning rate
of 0.001. The input layer is a vector with 240 elements. We
have used six fully connected hidden layers with the number
of nodes as 150, 140, 130, 120, 100 and 80, respectively.
The first layer will reshape the data into an 80 * 3 matrix. We
have added a dropout layer of 20% after every hidden layer.
The last layer will flatten the data and then run a softmax
function to calculate each class’s probability
