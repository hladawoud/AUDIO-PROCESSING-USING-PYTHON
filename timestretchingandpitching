#main packages
import librosa
import librosa.display
import IPython.display
import numpy as np
import matplotlib.pyplot as plt
from IPython.display import display
#loading the WAV file
filename = librosa.example('nutcracker')
y, sr = librosa.load(filename)
#printing the waveform and the sampling rate
print('waveform')
print(y)
print('\nsampling rate')
print(sr)
#ploting the original wave
fig, ax = plt.subplots(nrows=1, sharex=True)
librosa.display.waveshow(y, sr=sr)
ax.set(title='Envelope view, mono')
ax.label_outer()
#play the audio as an array
display(IPython.display.Audio(data=y, rate=sr))
#speed-up audio (compresses the audio to be twice as fast)
y_fast = librosa.effects.time_stretch(y, rate=2.0)
#slow-down audio (compresses the audio to half the original speed)
y_slow = librosa.effects.time_stretch(y, rate=0.5)
#pitch shift by -5, 5 octaves down (frequency and pitch decrease)
y_tritone = librosa.effects.pitch_shift(y, sr=sr, n_steps=-5)
#pitch shift by 5, 5 octaves up (frequency and pitch increase)
y_third = librosa.effects.pitch_shift(y, sr=sr, n_steps=5)
