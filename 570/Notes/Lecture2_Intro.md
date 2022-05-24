## 1.  Trade between Power & Rate & Error

### 1.1 Basic Concepts

- In practice, receiver integrate the power over Sine or Cosine

- There is always noise and interference



### 1.2 Probability of Error(P error)

**BPSK: Binary Phase shift Keying**

Assume noise is Gaussian：

Server sends X, Receiver receives Y

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge Y = X %2B N, N~N(0,\sigma^{2})"></div>

<div align=center><img width="800"  src="./File/Pictures/Week1/1.PNG"/></div>

SNR: Signal to noise ratio

A: amplitude of signal power

G: Noise Power

N: Noise

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge P_{error} = P(N>A) = Q(\frac{A}{G})=Q(\sqrt{2SNR})"></div>

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge A\uparrow \Rightarrow P_{error} \downarrow, G\uparrow \Rightarrow P_{error} \uparrow "></div>

### 1.3BPSK vs. QPSK

<div align=center><img width="800"  src="./File/Pictures/Week1/2.PNG"/></div>

**QPSK: Quadrature Phase shift Keying**

Setting the probability then we know the SNR and we know the power we need

BPSK: 1bit/Symbol

QPSK: 2bit/Symbol

Distance(d) represents power

<div align=center><img width="800"  src="./File/Pictures/Week1/2.PNG"/></div>

### 1.4Shannon Capacity Law for AWGN(additive white gaussian noise)

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge R = W \cdot \log(1 %2B SNR)"></div>

R: **Rate**( **Channel Capacity** in bits per second, a theoretical upper bound on the net bit rate(information rate))

W: Channel Bandwidth

log: Bad news

R increase **linearly** in W, but increase **logarithmically** in Power

n exponential increase in Power yields over a linear increase in Rate

<div align=center><img width="800"  src="./File/Pictures/Week1/5.PNG"/></div>

### 1.5 Bits per Symbol

**16 Symbols (16 QAM)**

Bits per Symbol = 4, since 2<sup>4</sup> = 16

**Most Common Modulation**: 256QAM(8bits/Symbol)

**Error Same:** Keep symbol's distance same

<div align=center><img width="800"  src="./File/Pictures/Week1/6.PNG"/></div>

<div align=center><img width="800"  src="./File/Pictures/Week1/7.PNG"/></div>

**64QAM = 2<sup>6</sup> : 6 bits/ symbol**

### 1.6 Summary: Rate & Symbol

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge Rate \propto  \log( number \hspace{1ex} of \hspace{1ex} symbol)"></div>

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge 2^{bit/symbol}=number \hspace{1ex} of \hspace{1ex} symbol"></div>

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge Power \propto  Amplitude^2 \propto (number \hspace{1ex} of \hspace{1ex} symbol)"></div>

**Amplitude is Twice** from 16 to 64

#### (a). Rate-Power Plot

<div align=center><img width="800"  src="./File/Pictures/Week1/8.PNG"/></div>

#### （b). Error-Power Plot

<div align=center><img width="800"  src="./File/Pictures/Week1/9.PNG"/></div>





## 2. Propagation

<div align=center><img width="800"  src="./File/Pictures/Week1/3.PNG"/></div>

Omnidirectional Antenna

Directional Antenna

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge P_{received-power} \propto \frac{Transmitted-Power}{Surface} \propto C \cdot P_t \cdot d^{-2} \propto  P_t \cdot d^{-n}"></div>

### 2.1 Simplified Path Loss Model

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge P_{received-power} =  P_t \cdot k \cdot (\frac{d_0}{d})^{n}"></div>

d<sub>0</sub> : the reference distance at which p<sub>r</sub> = k P<sub>t</sub>

### 2.2 "dB" Notation

Power is measured in Watts, 1mW in dB is 0dBm (m means milliwatt)

Because **10log<sub>10</sub>1mW = 0 dBm**

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge P_{r_{dBm}} =  P_{t_{dBm}} %2B k_{dB} - n \cdot 10\log_{10}(\frac{d}{d_0})"></div>

<div align=center><img width="800"  src="./File/Pictures/Week1/4.PNG"/></div>

### 2.3 Actual Situation: Shadowing & Fading

#### (a). Shadowing

**Variation due to large-scale obstruction and reflection**

<div align=center><img width="800"  src="./File/Pictures/Week1/10.PNG"/></div>

#### (b). **Multiple Fading**:

**Variation due to multiple paths (small-scale in the order of ware)**

constructive vs. destructive superposition of multiple reflections 

<div align=center><img width="800"  src="./File/Pictures/Week1/11.PNG"/></div>

**MIMO: multiple input & multiple output**

### 2.4 Two Famous Ways to Module the Mess:

#### (a) Log-Normal Model

##### (i) Definition

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge P_{r} =  P_t \cdot k \cdot (\frac{d_0}{d})^{n} \cdot \psi"></div>

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge \psi_{dB}=10 \log_{10} (\psi) \hspace{1ex}  ~ \hspace{1ex} N(0,\sigma^{2})"></div>

**SAI** is a random variable with a **Log-Normal Distribution**.

Log-Normal means 10log<sub>10</sub>(SAI) is normal distribution

##### (ii) Usage

Used for shadowing mostly in large-scale networks and sometime fading in small-scale network

##### (iii) Outage Probability

If my noise power is a constant, then if Pr<Pout, then the communication will not meet the specified error performance

Do not exceed the Pout(Threshold)

##### (iiii) Calculation

area = Probability under the threshold

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge P_{r(dBm)} =  P_{t(dBm)} %2B k_{dBm} -10\cdot n \log_{10}(\frac{d}{d_0}) %2B \psi_{dBm}"></div>

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge P_{outage} = P(P_r < P_{out})"></div>

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge = P(P_{t(dBm)} %2B k_{dBm} -10\cdot n \log_{10}(\frac{d}{d_0}) %2B \psi_{dBm} < P_{out(dBm)})"></div>

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge = 1 - P(\psi_{dBm} > P_{out(dBm)} - P_{t(dBm)} - k_{dBm} %2B 10\cdot n \log_{10}(\frac{d}{d_0})^{n} )"></div>

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge = 1 - Q(\frac{P_{out(dBm)} - P_{t(dBm)} - k_{dBm} %2B 10\cdot n \log_{10}(\frac{d}{d_0})}{\sigma_{\psi}})"></div>

Where Q assume N(0,1) - Look at table

so if we have X~N(u,sigma<sup>2</sup>), then (X-u)/sigma ~ N(0,1)

<div align=center><img width="800"  src="./File/Pictures/Week1/13.PNG"/></div>

<div align=center><img width="800"  src="./File/Pictures/Week1/12.PNG"/></div>

<div align=center><img width="800"  src="./File/Pictures/Week1/14.PNG"/></div>

#### (b) **Rayleigh**



##### (i). Definition

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge f_{Pr}(x) =  \frac{1}{P_r} \cdot e^{\frac{-x}{P_r}}"></div>

##### (ii). Usage

 used for fading 

##### (iii). Outage Probability

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge P_{outage} = P(P_r < P_{out}) = 1 - e^{\frac{-P_{out}}{P_r}}"></div>

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge P_r \geq \frac{P_{out}}{-\ln(1-T_{prob out})}"></div>

##### (iiii). Calculation

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge E(x) = \frac{1}{\lambda}"></div>

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge f_x(x) = \lambda e^{-\lambda x}"></div>

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge F_x(x) = 1- e^{-\lambda x}"></div>

Find Pr such that the outage probability is less than some threshold T

<div align=center><img width="800"  src="./File/Pictures/Week1/15.PNG"/></div>

<div align=center><img width="800"  src="./File/Pictures/Week1/16.PNG"/></div>

### 2.5 Real-time Situation

we need to transmit  at some Pt bigger than initially anticipated, and we need receive power bigger than anticipated to proactively handle the randomromres due to shadowing and fading

Fading margin: Pr - Pout

When we talk about a distribution, we think that the same experiment is performed several times

In practice, we use a link over time, and Pr changes over time

So the "channel"(fading and shadowing) change over time.

How fast?



Slow-fading case: Channel changes slowly, working and a bus blocks line of sight to basestation

Fast-fading case: Very fast fluctuation over time

Since Pr changes over time, I am interested the average Perror over time

We will compute the **expectation** of Perror instead of Perror since Perror(x) is a changing

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge E(P_{error}) = \lmoustache P_{error}(x) \cdot f_{Pr}(x)dx"></div>

Last week for a AWGN we found 

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge P_{error} = Q(\sqrt{2SNR})"></div>

so 

<div align=center><img src="https://render.githubusercontent.com/render/math?math=\Huge E(P_{error}) = \lmoustache Q(\sqrt{2SNR}) \cdot \frac{1}{\overline{SNR}} \cdot e^{-\frac{\overline{SNR}}{SNR}}"></div>



















