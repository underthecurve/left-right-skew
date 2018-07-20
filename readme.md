Note: I made the .gif using ImageMagick & a version of [Trammell Hudson](https://twitter.com/qrs/status/1018594931911397378)'s "Animated Horizontal Wipe" code: https://trmm.net/Animated_wipe#

Code for the two images is in [`code.ipynb`](https://github.com/underthecurve/left-right-skew/blob/master/code.ipynb)

```
convert \
   -loop 0 \
   -delay 7 \
   left_labeled.png \
   \( right_labeled.png -crop 10x0 \) \
   \( -clone 0 -crop 10x0 -reverse \) \
   output.gif

```