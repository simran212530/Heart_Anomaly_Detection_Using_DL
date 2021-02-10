# Heart Anomaly Detection by Analysing Stethoscope sounds using Deep Learning
Currently, there are two effective ways to monitor one's heart condition;
electrocardiogram (ECG) and echocardiogram. However, both methods are
relatively expensive for mass inspection and require technical expertise in using
them. Our goal is to develop a reliable, fast and low-cost system that can be
used by untrained frontline health workers or anyone with internet access, to help
determine whether an individual should be referred for expert diagnosis,
particularly in areas where access to clinicians and medical care is limited. This
will also help in early diagnosis of CVDs which will drastically decrease the
potential risk factors of these deaths [1].
In this work, we take stethoscope sounds and even waveforms recorded using
the microphone of a mobile phone as input and apply deep learning to the task of
automated cardiac auscultation, i.e. recognizing abnormalities in heart sounds.
We describe an automated heart sound classification algorithm that combines
the use of time-frequency heat map representations with a deep convolutional
neural network (CNN).

## Dataset 
The dataset is divided
into 2 sets depending on the sources from where it was collected. Set A
(set_a.csv) data was collected from the general public via the iStethoscope Pro
iPhone app and Set B (set_b.csv) from a clinical trial in hospitals using the digital
stethoscope DigiScope.
In this dataset there are 4 classes of heartbeat sounds:
1. Normal: healthy heart sounds
2. Murmur: extra sounds that occur when there is turbulence in blood flow
that causes the extra vibrations that can be heard
3. Extrahls: heartbeats with an additional sound
4. Extrasystoles: are additional heartbeats that occur outside the
physiological heart rhythm and can cause unpleasant symptoms


## Pre-Processing of the Data
The heart sounds recorded by digital stethoscope and the mobile phone
microphone often has background noise. The preprocessing of heart sounds is
an essential and crucial step for automatic analysis of heartbeat recordings. We
have cut out all the audio files that have a duration of fewer than 3 seconds
because they do not contain enough data points to accurately classify
heartbeats. The recordings have to be converted to some fixed length prior to
training, we slice the heart sounds into fixed-length segments of length 3 sec. To
increase the size of the dataset we are slicing large files into multiple smaller files
while still retaining their original label (i.e. normal or abnormal).



## To classify a heartbeat sound
The heartbeat audio file must be in .wav format
1. Download the repository
2. Open the terminal/command prompt and cd to the downloaded repository
3. Run the python script "testing.py"
        
        """ python testing.py heartbeat-to-classify.wav"""
        NOTE: Use Python3
        
4. The predicted class and the confidence will be displayed

Download the dataset from [here](http://www.peterjbentley.com/heartchallenge/index.html).
