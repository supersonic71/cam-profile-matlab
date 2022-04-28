# cam-profile-matlab
A matlab program to generate cam profiles for camshafts 

This program called ‘camplot.m’ was made in Matlab to generate cam profiles for
given up-stroke and down-stroke conditions.
This program supports many types of motions such as uniform motion, cyclic motion
and and simple harmonic motion.
The program also supports multiple types of motion for a single stroke – for example,
the first half of an upstroke can be uniform motion and the second half can be cyclic
motion.
The user only needs to input the stroke information in this format -
<disp> <motion type> in <angle from reference>
For example, 30 SHM in 90
will create a stroke from current location to 30 units displacement from the base
circle in 90 degrees.
The program automatically detects if given information refers to upstroke or
downstroke depending on previous data.
  
  Example 1          
Generate a camprofile of base radius 30 units. The upstroke is from 0 to 90 degrees in     
simple harmonic motion. The Dwell is from 90 degrees to 150 degrees. The        
downstroke is from 150 to 270 degrees in cyclic motion.         
Maximum displacement is 20 units.        
What user has to input is marked in bold -       
Enter base cicle radius : 30       
Enter segment : 20 shm in 90       
Enter segment : 20 uni in 150       
Enter segment : 0 cyl in 270       
Enter segment : 0 uni in 360       
The cam profile is then generated instantly. Note that by convention in Matlab 0        
degrees is in right hand side and this represents clockwise rotation.        
Different colours represents different strokes. The left is the displacement plot and       
right is the cam profile.         
  
![image](https://user-images.githubusercontent.com/17806210/165669397-86379f0e-9080-48ce-8a33-ae3c91e15ce8.png)

  
  
  
  Example 2

Generate a camprofile as follows -         
Upstroke – till 90 degrees. Half should be uniform motion and rest simple harmonic        
motion.       
Dwell – 90 to 130 degrees.       
Downstroke – till 270 degrees. Till 170 degrees it should be cyclic and rest should be       
uniform motion.       
As before, user input is given in bold :        
Enter base cicle radius : 30    
Enter segment : 10 uni in 45     
Enter segment : 20 shm in 90     
Enter segment : 20 uni in 130     
Enter segment : 10 cyl in 170     
Enter segment : 0 uni in 270     
Enter segment : 0 uni in 360        
  
![image](https://user-images.githubusercontent.com/17806210/165669443-4f8b3d2a-ea28-44cc-8f78-76ac6e054a56.png)        
