Here’s an improved and more structured version of your problem description:

---

## Audio Modulation: Problem Description

### Objective
The goal of this project is to record three audio samples, apply Low Pass Filtering (LPF) to limit their frequency range, and then modulate them using Single Sideband (SSB) modulation on different carrier frequencies. The samples will then be demodulated to recover the original signals. This process will adhere to the Nyquist Theorem, ensuring proper signal sampling and modulation.

### Step 1: Gathering Test Samples
I recorded my voice three times, each recording lasting 10 seconds. The sampling frequency was set to 48,000 Hz, chosen for the following reasons:

1. It supports a wide range of carrier frequencies while satisfying the Nyquist theorem.
2. It is a standard sampling rate in many audio applications.

### Step 2: Limiting the Frequency
To limit the frequency of the recorded samples, I applied a Low Pass Filter (LPF). I had two options for the LPF design:

- **Chebyshev Type I Filter**
- **Butterworth Filter**

I chose the **Chebyshev Type I** filter because of its sharper roll-off compared to the Butterworth filter. However, this choice introduces a ripple in the passband, which can be controlled by specifying the ripple amount. I experimented with several cutoff frequencies: 4000 Hz, 3700 Hz, and 3500 Hz. After testing, I found that a cutoff frequency of **3500 Hz** provided the best balance between clarity and preservation of the voice’s details, which led me to select it as the final choice.

### Step 3: SSB Modulation
For the SSB modulation process, I selected the following carrier frequencies: **10 kHz**, **15 kHz**, and **20 kHz**. These carrier frequencies were chosen to satisfy the Nyquist condition and ensure proper bandwidth distribution. Given that we are not using practical filters, each signal’s bandwidth was chosen to be 5 kHz.

### Step 4: SSB Demodulation
After modulating the signals, I proceeded with SSB demodulation to recover the original samples. The demodulation process successfully recovered the signals
