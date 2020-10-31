#The Row Beneath

We download the image file.

Nothing of interst from`exiftool`.

A quick scan through the image with `stegsolve` also displays nothing obvious;

Let's see if there are any strings hiddden in it;

```
[jaxigt@MBA the_row_beneath]$ strings -n 10 plan.png 
'9=82<.342
!22222222222222222222222222222222222222222222222222
CYCTF{L00k_1n_th3_h3x_13h54d56}
```
Bingo!

## CYCTF{L00k_1n_th3_h3x_13h54d56}
