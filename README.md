# NQWWVC
(Not Quite) the Worlds Worst Video Card

This is a GAL based implementation of Ben Eater's "Worlds Worst Video Card", with all the logic needed to display an image from a flash ROM, minus the ROM itself and a clock signal. Instead of 20 chips, it's just 4. Two of those are identical 10 bit counters, one for horizontal, the other for vertical. The other two chips are essentially comparators, one looks at the horizontal counter output and produces an output when the count is in the correct range, the other does the same thing for the vertical counter. The basic idea for both is the same, but the values they produce their sync pulse from is different. Each also has a flip flop in code, rather than using a built in D-type. I honestly can't remember why now...
