# Computer-Vision_Linear-Scaling-and-Histogram-Equalization
Linear Scaling and Histogram Equalization using Luv domain

## I. Purpose
1. To perform linear scaling and histogram equalization in Luv domain, using a small window.
2. Input parameters are following:
   	w1 h1 w2 h2 input-image output-image

## II. Files List
`prog_1.py` --- Program that performs Linear scaling, by converting the given image to Luv format and then scaling the values of L, and then converting it back to rgb format to display the image.

`prog_2.py` --- Program that performs histogram equalization by converting the given image to Luv format and then equalizing it using the lookup table, and then converting it back to rgb format to display the image.

`prog_3.py` --- This program is similar to prog_1 but it performs Linear scaling in xyY domain

Output images --- All 3 programs were tested with 4 set of test images, results are available in `Output_images` folder
  

## III. How to Run the Program:
Python 3 Version
Open a terminal, go to the current path. 
Example :  `python3 prog_1.py 0.5 0 1 1 test_a.bmp output_1a.bmp`

## IV. Output:    
The program will print the scaled image and eqalized image, along with the values of RGB and Luv for each pixel of the input image.

## V. Handling of any kind of errors(like division by zero, etc):
1. By using hallucinated constant 0.01 and adding it to value of L, in order to avoid divide by 0 error, or zero by zero error. In xyZ try-catch block is used to handle divide by zero error.  
2. By applying conditions to values of r, g, b.   
Condition like checking NaN error, if it is met, the values(r,g,b) are equated to 0.  

## Sample Result
![Result](https://github.com/nand6m/Computer-Vision_Linear-Scaling-and-Histogram-Equalization/blob/master/Output_images/sample_results.png)
