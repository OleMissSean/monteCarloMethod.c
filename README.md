CSci423.Assignment3.c
=====================

Assignment #3 for CSci423: Operating Systems. 

CSCI423 Programming Assignment 3

An interesting way of calculating pi is to use a technique known as Monte Carlo,
which involves randomization. This technique works as follows: Suppose you have a
circle inscribed within a square, as shown in the following figure (Assume that the
radius of this circle is 1.) First, generate a series of random points as simple (x, y)
coordinates. These points must fall within the Cartesian coordinates that bound the
square. Of the total number of random points that are generated, some will occur
within the circle. Next, estimate pi by performing the following calculation:
  pi = 4 * ( number of points in circle ) / ( total number of points )
Write a multithreaded C program of this algorithm that creates several threads, each
of which generates random points and determines if the points fall within the circle.
Each thread will have to update the global count of all points that fall within the
circle. Protect against race conditions on updates to the shared global variable by
using mutex locks. After all these threads exit, the parent thread will calculate and
output the estimated value of pi. It is worth experimenting with the number of
random points generated. As a general rule, the greater the number of points, the
closer the approximation to PI. So the total number of points generated by all the
threads should be no less than 50,000,000.
(0,0)
(-1,-1) (1,-1)
(-1,1) (1,1)
