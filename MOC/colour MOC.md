(I don't really have anything specific in this yet so I'm just gonna input whatever)

# basic biology
## retina
Human eyes have this thing called <a href="https://en.wikipedia.org/wiki/Retina">retina</a>
![[Pasted image 20250917181901.png]]

Inside the retina, there are around __6-7 million__ __cones__

## cone
For humans, there are 3 types of <a href="https://en.wikipedia.org/wiki/Cone_cell#Distribution">cone</a>:
- L: most sensative at around 560nm (yellow->red)
- M: most sensative at around 530nm (green->yellow)
- S: most sensative at around 420nm (blue)

The distribution of cones vary a lot based on people, but the general pattern suggests:
- $L\geq M> S$
- $S\approx 2\%$ overall

# colour theory (math)
## sensitivity of cone
The sensitivity cannot be expressed as a function, but it can be approximated using a normal curve
![[Pasted image 20250917183353.png]]
Where for $X\sim N_{\text{not actually a normal distribution}}(\mu,\sigma)$:
$\displaystyle L\sim N(570, 50) \to l(\lambda)=\exp\left( - \frac{(\lambda-570)^2}{2(50^2)} \right)$
$\displaystyle M\sim N(540, 40) \to m(\lambda)=\exp\left( - \frac{(\lambda-540)^2}{2(40^2)} \right)$
$\displaystyle S\sim N(450, 20) \to s(\lambda)=\exp\left( - \frac{(\lambda-450)^2}{2(20^2)} \right)$

Where $\lambda$ is the wavelength in nanometer, $l,m,s$ are __spectral sensitivity functions__.
(Note they are not exactly PDFs of a normal distribution, as they do not divide by the factor $\displaystyle \frac{1}{\sigma \sqrt{ 2\pi }}$)

## what does that mean? (in math/probability)
When our eyes get struck by a beam of light, the cones receive photons, and each photon has a chance to be activated.
And that chance, is (mostly) dependent on the corresponding cone spectral sensitivity function

_example_ (probability to be activated)
For example, if a beam of colour green (individual photons of wavelength $530nm\leq\lambda\leq570nm$) struck to my eye,
- The L cones have a sensitivity of around $r_{L}=\displaystyle \int_{530}^{570}l(\lambda)d\lambda \approx 36.11$
- The M cones have a sensitivity of around $r_{M}=\displaystyle \int_{530}^{570}m(\lambda)d\lambda \approx 37.31$
- The S cones have a sensitivity of around $r_{S}=\displaystyle \int_{530}^{570}s(\lambda)d\lambda \approx 0.001588$

To find the actual __probability for a cone to be activated__, we find the cone's sensitivity's ratio from the total sensitivity:
- The chance for an L cone to be activated: $\displaystyle P(L)= \frac{36.11}{36.11+37.31+0.001588}\approx 49.18\%$
- The chance for an M cone to be activated: $\displaystyle P(M)= \frac{37.31}{36.11+37.31+0.001588}\approx 50.82\%$
- The chance for an S cone to be activated: $\displaystyle P(S)= \frac{0.001588}{36.11+37.31+0.001588}\approx 0.0000002163\% \approx 0$

_example_ (probability to be activated and perceived)
Given previous example's result for probabilities to be activated
If we consider the expected value, assuming one has 6 million cones with
- L: 3.60 million cones (60%)
- M 2.28 million cones (38%)
- S: 0.12 million cones (2%)

Note that given this, the chance for a single photon to be activated (before entering a specific cone) is:
$$
\text{chance to be enter the cone} \times\text{chance to to be activated by the cone}
$$
Where from the current setup:
$$
\text{chance to activate green cone} = 0.60*0.4918=0.29508
$$
In other words, from this setup, the chance for you to __perceive a tiny amount of green__ from one single photon is around $29.508\%$

Note that this little tiny amount does almost nothing to you, to actually perceive the colour, you might need much much more photons (exact number is left for the reader to research because the writer is not able to find the value)

_example_ (expected colour to be perceived)
Then, when a beam of light of around $3\times 10^{18}$ photons per second struck your eyeball, they will enter to cones __almost randomly__, thus, we expect to perceive
- $E(L)=3*10^{18}*0.60*0.4918=8.85*10^{17}$ photons per second
- $E(M)=3*10^{18}*0.38*0.5082\approx 5.79*10^{17}$ photons per second
- $E(S)=3*10^{18}*0.02*0.0000002163\approx 0.2978*10^{10}$ photons per second

