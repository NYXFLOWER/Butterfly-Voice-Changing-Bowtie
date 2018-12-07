QUESTION 1 (worth up to 5 marks)
Provide a screenshot of [wsprobe∼] for a typical voiced sound, and explain the features
in the waveform and spectrum that distinguish it from an unvoiced sound. Hint: use the
‘snapshot’ feature in [wsprobe∼] to obtain a static display.

Answer:

When voiced sounds are produced, the vocal cords vibrate, or, opens and closes, in a certain frequency. The speaker has to put in more energy than unvoiced sounds. It is shown in the waveform as periodic wave patterns with a relatively higher amplitude and intervals indicating a closure of the vocal cords. In the spectrum, a voiced sound can be detected where there appear several peaks at the low-frequency end, indicating formants generated when soundwave resonates in the human vocal tract. After those peaks, the frequency drops dramatically, showing that the energy decays after pronouncing the voiced sound.

QUESTION 2 (worth up to 5 marks)
Which sounds are most affected when the low-pass cut-off frequency is set to around 500
Hz - vowels or consonants - and why?

Consonances. Vowels are all voiced sounds whose frequency are low, meaning that most of these signals will pass the filter, whereas many consonances are unvoiced sounds with high frequency which may be cut off by the low pass filter with a cut-off frequency at 500Hz.

QUESTION 3 (worth up to 5 marks)
How is it that the speech is still quite intelligible when the high-pass cut-off frequency is set to 10 kHz?

Answer：

Consonances carry more information 

Firstly, as it is discussed in Question 2, vowels and some low-frequency consonances will be cut-off by the high-pass filter. It is believed that consonances carry more information than vowels and most of them are retained in this case.

Secondly, the speech is intelligible partially because human brain has a scheme which automatically supplement missed language information in the speech during processing the language signals. Additionally, having known the content of the speech, in this case,  helps the brain to supplement and predict the information.

The quality of the filter also affects the result. It is widely discussed by users that the high-pass filter in Pd has unsatisfactory quality. In this case, some low-frequency signals may not be filtered.

QUESTION 4 (worth up to 5 marks)
COM3502-4502-6502: The [GraphicEqualiser∼] object uses an FFT internally; what does FFT stand for and what does an FFT do?
COM4502-6502 ONLY: What is a DFT and how is it different from an FFT?

Answer: 

FFT stands for Fast Fourier Transform. In signal processing, the Fourier transform is the frequency domain representation of the original signal, ie. the spectrum. The complex spectrum represents the amplitude and phase of the original signal. 

The Fast Fourier Transform (FFT) is an algorithm for computing the Discrete Fourier Transform (DFT). Fourier Transform is a continuous function whereas, in digital signal processing, only a finite number of samples in a finite time sequence can be processed. Thus Fourier Transform goes discrete. The DFT computes the spectrum at N evenly spaced discrete frequencies. FFT differs from DFT in computational complexity, which is O(n log n) for the former and O(n*n) for the latter.



QUESTION 5 (worth up to 10 marks)
With speed = 50 and depth = 0.5, what are the minimum and maximum amplitudes of your LFO output, and how do they vary with changes in these two settings? Also, please provide two screenshots: (a) your [LFO∼-help] object and (b) the internal structure of your [LFO∼] object.

Answer:

The minimum amplitude of the LFO output  is -0.5 and the maximum amplitude is 0.5. The range of amplitude equals to and changes with the range of depth, which is [-depth, +depth]. Altering the speed change the frequency of the original signal without affecting the amplitude.

QUESTION 6 (worth up to 5 marks)
In your own words16, why is this effect known as ‘ring modulation’?

Answer:

This effect is achieved by the source signal being modulated by another sound wave, typically a sine wave. It adopts a signal processing function in electronics named Ring Modulation, coming from the ring-like shape of the analogue circuit of diodes.

QUESTION 7 (worth up to 5 marks)
Why is SSB commonly used in long-distance radio voice communications?

Answer:

Long-distance radio voice communication requires larger bandwidth and more power. By using SSB, signals on one sideband is filtered, reducing the power wasted on a carrier as well as the pressure of bandwidth increase. With signals on one sideband being filtered, the communication quality is increased with less distortion.

QUESTION 8 (worth up to 5 marks)
COM3502-4502-6502: Why can the voice be shifted up in frequency much further than it can be shifted down in frequency before it becomes severely distorted? /emphHint: look at [wsprobe∼].
COM4502-6502 ONLY: Your frequency shifter changes all the frequencies present in an input signal. How might it be possible to change the pitch of a voice without altering the formant frequencies?

Human hearing has a range of about 20 Hz to 20,000 Hz. The human voice has a fundamental frequency ranging from 85 Hz to 255 Hz, basically in the low-frequency area. A small change in this area will make a big difference in the feeling of the listener such as the sex and timbre of the speaker, leading to a feeling of a severe distortion. Consequently, the range can be shift down is smaller than that can be shift up before a server distortion.

It is possible to change the pitch of a voice without altering the formant frequencies by adopting an algorithm (such as linear prediction) to separate the fundamental frequency and the formants. After the separation, the fundamental frequency can be shifted individually and then be merged with the unchange formants signals. It canbe done using the combination of high-pass and low-pass filters or the Graphic Equaliser in Pd.

QUESTION 9 (worth up to 5 marks)
In a practical system, why is it important to keep the feedback gain less than 1?

Answer:

The value of the feedback gain mainly affects the amplitude and the overlap of the voice. When it is set greater than 1,  as the output of the feedback is repeatedly added to the source signal, the amplitude and the sound overlap will increase dramatically. It should be scaled appropriately to prevent damaging the hardware and the users' ears.