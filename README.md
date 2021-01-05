# Playlist Recommender - Predict Genre and Mood of audio files #
A helper model to assist music website to accurately predict the genres and mood.

Now a days everything is about personalization, which has increased the number of researches and work done using Deep Learning in Music Information Retrieval (MIR) field. 
The valence and genres of music plays significant role  in music recommendation system. This project aimmed to assist music website to accurately recognize the genres and 
valence of audio files by using models like -CNN, RCNN, CNN-LSTM and CNN-GRU. 

##Data & Features## </br>
Creted dataset by extracting 30-second music audios from Free Music Archive (FMA). It includes 5 music genres of 'Rock', 'Pop', 'Folk', 'Instrumental', and 'Electronic'. 
Used librosa library to extract features of each audio clip like Mel-spectrogram and Mel-Frequency Cepstral Coefficients (MFCC) as inputs. 
Feature Selection :Used Mel-spectrogram and MFCC because the frequency bands are equally spaced on the mel scale, which approximates the human auditory system’s response


Motivated by the work of Keunwoo Choi, I have used  Yu et al , Choi et al , for building our base models 

**Model Spec** </br>
Trained 5 different models with different number of convolution layers, FC layer , nodes, features like – MFCC & Mel-Spectrograms and adding LSTM and GRU layers. 
The models uses 4-5 number of convolutional layers, Learning rate = 0.001, l2 lambda =0.002, Batch size = 75, 
TimeDistributed wrapper layer outside flatten layer for LSTM, 1 LSTM layer, 2 GRU layers with regularized flattened and batch normalization every layer. 
