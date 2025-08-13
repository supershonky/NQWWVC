# NQWWVC
(Not Quite) the Worlds Worst Video Card

This is a GAL based implementation of Ben Eater's "Worlds Worst Video Card", with all the logic needed to display an image from a flash ROM, minus the ROM itself and a clock signal. Instead of 20 chips, it's just 4, all are ATF22V10C - the faster the better. Two of those are identical 10 bit counters, one for horizontal, the other for vertical. The other two chips are essentially comparators, one looks at the horizontal counter output and produces an output when the count is in the correct range, the other does the same thing for the vertical counter. The basic idea for both is the same, but the values they produce their sync pulse from is different. Each also has a flip flop in code, rather than using a built in D-type. I honestly can't remember why now...

As all the chips are ATF22V10C's, a final circuit is quite power hungry - approximately 400mA at 5V using 7ns chips.

I tested this with an LG Full HD TV/Monitor that happened to have a VGA input. It worked, with a more stable image than Ben Eater's discrete logic version. That said, I have not done any extensive testing, so use at your own risk. It's down to you to get the right clock frequency and hook the chips up correctly. I accept no responsibility if you destroy a rare and precious CRT as a result!

Ultimately, I have made these files available as examples of WinCUPL code.
