# Common Radar Signal Mask Functions (CW, LFM, HFM, Bark, Costas) [with MATLAB Code]

1. CW signal:
   - Conventional radar signals generally refer to those with constant phase, which are quite common in pulsed radar systems. In single carrier frequency signals, the phase is constant and corresponds to c(t) = 0, as shown in the following signal model expression:

Simulation results:
2. LFM signal:
   - LFM (Linear Frequency Modulation) signals are widely used in radars. Their phase function changes quadratic with time: c(t) = πkt², where k represents the slope of the waveform's frequency modulation, B = kT denotes the signal's bandwidth, and T represents the pulse width. The bandwidth B determines the resolution that can be achieved. The LFM signal model is as follows:

Simulation results:
3. HFM signal:
   - HFM (High Frequency Modulation) signal expression:
     Here, T is the pulse width, b = -k / f1 f2 is the signal's frequency modulation parameter, k = B / T is the corresponding linear frequency modulation slope, B is the signal bandwidth, f0 is the waveform's center frequency, f1 = f0 -B / 2 is the lower frequency limit, and f2 =f0 +B / 2 is the upper frequency limit.

Simulation results:
4. Bark encoding signal:
   Bark sequence achieves an ideal non-periodic autocorrelation function. The general expression for a phase-encoded radar signal is as follows:

   Here, u(t) = a(t) e jφ(t), where u(t) is its envelope, φ(t) is the phase modulation function, and a(t) is the amplitude modulation function; f0 is the carrier frequency.

For Bark code radar, take:

   Here, τ is the pulse width; τC is the width per code unit; N is the number of code units.

Each code unit's subpulses have their phase randomly selected from 0 or π relative to a continuous wave reference signal, usually marking "1" or "+" for phase 0 and "0" or "-" for phase π. For each code unit, its φ(t) ∈ (0, π). The coding rule for a 13-bit Bark code is shown in Figure 1.

Simulation results:
5. Costas frequency encoding signal:
Costas frequency encoding signals have multiple frequencies that shift according to a Costas sequence, each appearing only once and lasting the same duration. In this paper, the length of the Costas sequence is set to 16, resulting in the following sequence: {1, 10, 15, 14, 4, 6, 9, 5, 16, 7, 2, 3, 13, 11, 8, 12}. The relationship between time and frequency can be expressed using an M-order permutation matrix AM × M = {aij} (aij = 0 or 1).
In the formula: M is the length of Costas sequence; fm is the frequency after Costas sequence Cm modulation, f m = Cm ⋅ Δf, Δf is the frequency interval; tb is the pulse duration. um (t) is a sub-pulse, its calculation formula is
Simulation results:
MATLAB code:
close all; clear all; clc;\n​\nT = 0.26;\nfs = 20e3;\nfc = 1e3;\nB = 1000;\nt = 0:1/fs:T-1/fs;\n​\ntype_index = 5; \ntype_name = {'PCW', 'LFM', 'HFM', 'Bark', 'Costas'};\n​\nswitch type_index\n    case 1\n        % 1. pcw\n        x = exp(1i*2*pi*fc*t);\n        \n    case 2\n        % 2. lfm\n        k = B/T;\n        f0 = fc-B/2;\n        x = exp(1i*2*pi*(f0*t+k/2*t.^2));\n\n  

## Images

![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](01.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](02.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](03.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](04.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](05.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](06.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](07.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](08.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](09.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](10.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](11.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](12.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](13.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](14.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](15.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](16.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](17.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](18.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](19.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](20.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](21.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](22.jpg)
![Common radar signal ambiguity functions (CW, LFM, HFM, Bark, Costas) [with MATLAB code]](23.jpg)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
