# HappyNumbersOutput
This holds the text output for the happy numbers project done in 2011


In the prototypical case, we consider base-10 representation of a number n, and we let H(n) be the sum of the squares of its base-10 digits.  We then iterate H until it cycles (cycles are inevitable since a d-digit number has H(n) <= 81d, which will be less than n if d is sufficiently large).  The cycles of this map are:

0 --> 0,  and
1 --> 1,  and
4 --> 16 --> 37 --> 58 --> 89 --> 145 --> 42 --> 20 --> 4

We can canonically identify each cycle with its smallest element (e.g., 0, 1, 4).  This then partitions the natural numbers into numbers which eventually reach 0 (called type 0 numbers), numbers that reach 1 (called type 1 numbers **also called happy numbers**), and numbers that reach 4 (called type 4 numbers).


We want to enumerate how many m-digit numbers are of each type.  And!  We also want to generalize this to other functions H(n) (and other bases).


For instance!  We could say base b, exponent k to mean that H(n) is the sum of the base-b digits of n when each is raised to the k.
Or more generally, we might write something like  H(n) = a0, a1, a2, a3, ..., a9  to mean that H(n) is what happens when you replace each (base-10) digit, X, of n with aX and then add these up.  For instance  H(4204) = a4+a2+a0+a4.

Each fixed map H gives us a finite set of cycles, which we can canonically identify with their smallest element, and thus it partitions the natural numbers into a finite number of types (based on which cycle they go to).



Now!!!  The format for the output files is that every line of each file is of the form:

m   x

where m is the line number, and x is the number of non-negative integers having at most m base-b digits of the given type.


The TYPE in question (and the map H) is determined by the naming convention of the file in a self-explanatory way.
