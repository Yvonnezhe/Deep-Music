# Deep Music

## Results
See the .mid files in the samples folder for examples of artificial music generated by our model.

## Installation
Requirements:
- [TensorFlow](https://www.tensorflow.org/versions/r0.11/get_started/os_setup.html#download-and-setup)
- [Keras](https://keras.io/#installation)
- [Python MIDI](https://github.com/vishnubob/python-midi): pip install python-midi
- [h5py](http://docs.h5py.org): conda install h5py

## MIDI Input Details
Every input vector x is 66-dimensional and structured as follows:
- x[0]: relative event time from previous input (tick)
- x[1]: BPM
- x[2-5]: Channel 1: font, note, velocity, duration
- x[6-9]: Channel 2
- ...
- x[62-65]: Channel 16

In MIDI, an event is characterized by the following features:
- Font: Integer in [0,127]
- Note: Integer in [0,127]
- Velocity: Integer in [0,255]
- Duration: Integer in (0,infinity)

Notes:
- We use a -1 in all features to indicate a silenced channel.
- The 16 channel font features are fixed for the full duration of a single track.
- The BPM is fixed for the full duration of a single track.

## Resources
* [The Neural Network Zoo](http://www.asimovinstitute.org/neural-network-zoo/)

* [Analyzing Six Deep Learning Tools for Music Generation](http://www.asimovinstitute.org/analyzing-deep-learning-tools-music/)

* [Composing Music With Recurrent Neural Networks: Theory](http://www.hexahedria.com/2015/08/03/composing-music-with-recurrent-neural-networks/)
* [Composing Music With Recurrent Neural Networks: Code](https://github.com/hexahedria/biaxial-rnn-music-composition)
* [Composing Music With Recurrent Neural Networks: Extensions](http://www.hexahedria.com/2016/08/08/summer-research-on-the-hmc-intelligent-music-software-team)

* [Magenta: Blog](https://magenta.tensorflow.org/)
* [Magenta: Code](https://github.com/tensorflow/magenta)

* [Keras](https://keras.io/)
* [Sequence to Sequence Learning with Keras](https://github.com/farizrahman4u/seq2seq)

* [About MIDI](http://stackoverflow.com/questions/14448380/how-do-i-read-a-midi-file-change-its-instrument-and-write-it-back)
* [Python MIDI Library](https://github.com/vishnubob/python-midi)

* [Free MIDI Files](http://www.mididb.com/genres/)
