# speech_recognition_challenge

The dataset is a reduced version of the [`TensorFlow Speech Commands Dataset`](https://www.tensorflow.org/datasets/catalog/speech_commands) and contains audio waveforms of the words:
- `down`, 
- `go`, 
- `left`, 
- `off`, 
- `on`, 
- `right`, 
- `stop`, 
- `up`.

The speech is a time series signal and a well known strategy for extracting a good representation of the raw audio is to mimic the processing of the auditory system of the humans. A well established feature representation for speech is the so called "log mel-spectrum". This feature in fact, takes into account how humans perceive both the frequencies and the amplitude of the sound logarithmically.

![auditory-system](https://www.researchgate.net/profile/Morteza_Khaleghi_Meybodi/publication/322343133/figure/fig1/AS:581011472093184@1515535337239/Figure-31-Schematic-of-the-auditory-system-with-its-primary-components-including.png)


For this project these features are precomputed: for each audio waveform of 1 sec duration, the log mel-spectrum is a bi-dimensional representation (frequency vs time) of shape [128, 32]. Here, we first resize the "image" into a [32, 32] matrix and then we flatten the representation into a 32x32 = 1024 vector.