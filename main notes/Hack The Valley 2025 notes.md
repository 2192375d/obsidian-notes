![[Pasted image 20251004122207.png]]
![[Pasted image 20251004122223.png]]

# plans (post 1:30 am)
- Get more animals done (expected to be 20, or as much as possible)
- Add curl ()
- Get animal documentations done
- Convert the hyperspectral image to LMS, and do curl
- Consider making a program that estimates UV using math

# animals (in the 20)
old ones:
- cat, dog, sheep, goat, pig, cow

new ones:
- ~~rat, horse~~, rabbit, panda, squirrel, elephant, lion, wolf, fox, bear, racoon, deer, kangaroo, tiger


| animal   | LM cone $\lambda$ | S cone $\lambda$ | source                                                                                                                         |
| -------- | ----------------- | ---------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| cat      | 561               | 454              | https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0147318 (see also photopic spectral sensitivity of the cat)  |
| dog      | 555               | 429              | https://www.sciencedirect.com/science/article/pii/S0042698905004548                                                            |
| sheep    | 552.2             | 445.3            | https://www.neitzvision.com/research/publications/publications/1998-Jacobs-Dichromacy_cows_goats_sheep-VisNeuro.pdf            |
| goat     | 552.5             | 443.3            | https://www.neitzvision.com/research/publications/publications/1998-Jacobs-Dichromacy_cows_goats_sheep-VisNeuro.pdf            |
| pig      | 556.7             | 440.7            | https://www.neitzvision.com/research/publications/publications/1998-Jacobs-Dichromacy_cows_goats_sheep-VisNeuro.pdf            |
| cow      | 555.3             | 451.3            | https://www.neitzvision.com/research/publications/publications/1998-Jacobs-Dichromacy_cows_goats_sheep-VisNeuro.pdf            |
| rat      | 502               | 362              | https://journals.plos.org/plosone/article?id=10.1371%2Fjournal.pone.0147318&utm_source=chatgpt.com                             |
| horse    | 539               | 428              | https://jov.arvojournals.org/article.aspx?articleid=2121452                                                                    |
| rabbit   | 520               | 425              | https://newrabbitowner.com/how-rabbits-see-the-world/                                                                          |
| panda    |                   |                  |                                                                                                                                |
| squirrel | 525               | 440              | https://pubmed.ncbi.nlm.nih.gov/6641841/                                                                                       |
| elephant | 552               | 419              | https://pmc.ncbi.nlm.nih.gov/articles/PMC1449733/                                                                              |
| lion     |                   |                  |                                                                                                                                |
| wolf     | 555               | 431              | https://www.researchgate.net/publication/231897541_Photopigments_of_dogs_and_foxes_and_their_implications_for_canid_vision/pdf |
| fox      | 555               | 431.5            | https://www.researchgate.net/publication/231897541_Photopigments_of_dogs_and_foxes_and_their_implications_for_canid_vision/pdf |
| bear     |                   | 440              | https://pubmed.ncbi.nlm.nih.gov/16572322/                                                                                      |
| racoon   |                   |                  | https://link.springer.com/article/10.1007/BF00223965                                                                           |
| deer     | 537               |                  | https://pubmed.ncbi.nlm.nih.gov/8006855/                                                                                       |
| kangaroo | 539               | 420              | https://www.sciencedirect.com/science/article/pii/S0042698999002102 ; https://academic.oup.com/mbe/article/20/10/1642/1164127  |
| tiger    |                   |                  |                                                                                                                                |

## What it does
Given an input image, video, or literally live webcam video, our project shows you how this vision looks like from the eyes of 30+ unique animals.
Provide built-in AI feature that explains how and why individual animals see the world in this way.

## How we built it
### for dichromatic animals (contributed by Tina and Lumiere)
Most of the dichromatic animals are done through:
1. remapping the pixels from human's persepective to specific animals', using the following matrix multiplication:
$$
\begin{bmatrix}
a &1-a &0 \\
a &1-a &0 \\
0 &0 &s
\end{bmatrix}
\begin{bmatrix}
L \\
M \\
S
\end{bmatrix}
=
\begin{bmatrix}
L_{animal} &M_{animal} &S_{animal}
\end{bmatrix}
$$
where $a$ and $s$ are values based on the two wavelengths which animals are sensitive to
2. adding a new acuity blur or anisotropic acuity blur with streak on top to mimic animals that have a more blur vision than humans
3. adding extra functionalities dedicated for that animal (eg for rat, the B cones are more sensitive on the top part of the sight, which means blues are easier to be perceived from the above of rat)

### for UV required animal (contributed by Kevin)

### for frontend (contributed by Yoshixi)
We built with a simple frontend that used progressive web app to have access to mobile microhpone and camera. We use websockets in socket.io to enable two-way communication for video streaming. Gemini was also used to provide tips.

## Challenges we run into
### Represent UV colour for "human" to see
Because human cannot see UV colour (at all), but animals can, so it's technically "impossible" for us to mimic the vision of any animals that can see UV light.
This is problematic because a LOT of animals can see UV light and skipping this just means we have to give up a good chunk of nice animals to mimic.
We managed to overcome this challenge by running a ML model that \[Kevin input stuffs here\]

### Changing the FOV (field of view)
\[stuffs with regards to challenging to change the shape\]

## what are we proud of...?
Literally everything we built so far! One day + night without sleep allowed us to achieve in everything we have so far
Managed to adapt 30+ different animals for the user to view.
The front end interface that works great with both mobile app and desktop, and our decent fps for best of user's experience

## What's next for A second view
We want to be able to add night vision and more FOV functionalites for other animals, eg horse with 360 degrees.

We seek to improve our pipeline and lower generation and video streaming latency time

## Documentation
https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0147318
https://www.sciencedirect.com/science/article/pii/S0042698905004548
https://www.neitzvision.com/research/publications/publications/1998-Jacobs-Dichromacy_cows_goats_sheep-VisNeuro.pdf
https://journals.plos.org/plosone/article?id=10.1371%2Fjournal.pone.0147318&utm_source=chatgpt.com
https://jov.arvojournals.org/article.aspx?articleid=2121452
https://newrabbitowner.com/how-rabbits-see-the-world/
https://pubmed.ncbi.nlm.nih.gov/6641841/
https://pmc.ncbi.nlm.nih.gov/articles/PMC1449733/
https://www.researchgate.net/publication/231897541_Photopigments_of_dogs_and_foxes_and_their_implications_for_canid_vision/pdf
https://pubmed.ncbi.nlm.nih.gov/16572322/
https://link.springer.com/article/10.1007/BF00223965
https://academic.oup.com/mbe/article/20/10/1642/1164127