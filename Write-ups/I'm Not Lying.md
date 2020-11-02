# I'm Not Lying

![Category](http://img.shields.io/badge/Category-Forensics-orange?style=for-the-badge) ![Points](http://img.shields.io/badge/Points-450-brightgreen?style=for-the-badge)

This time we're given an Audio file! We download and have a listen.

It seems to be audio dialog from a video. in deed it is... [this video](https://www.youtube.com/watch?v=CITrqyliiUM) to be exact;

Next we open the file in Sonic Visualiser and take a loook at the Spectogram View to see if the flag is deisplayed there (you could also do this in Audacity or any other app which can display audio Spectographic information).

![image](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/im_not_lying_specteral_analysis.png)

There's no visible flag here but you can see some off lines... particularly around 14800Khz

![image](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/im_not_lying_cyctf_spectrum.png)

This looks like morse code!

If we start decoding the first few dots and dashes we can see taht this looks promising!

![image](https://github.com/CTSecUK/CyberYoddha-CTF-2020/blob/main/images/im_not_lying_cyctf_morse.png)

At this point we tried many methods of extracting the audio at the relevant frenquency and then running it through various tools to try and decode the morse code automatically, but none of these tools was able to cleanly and correctly determine the flag, so in the end one of our team manually decoded it using the visiaul spectogram output.

The result was `CYCTFTRU7HH1DD3NUND3RL!E`

We add a few underscores to seperate the words and add the curly braces and we get our flag;

## CYCTF{TRU7H_H1DD3N_UND3R_L!E$}
