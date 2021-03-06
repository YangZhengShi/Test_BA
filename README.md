### Bundle Adjustment problem in MATLAB.

This code implements Bundle Adjustment using the Matlab function "lsqnonlin".

##### Description
In the main file a set of points and cameras are randomly generated being the
points distributed on a plane and the cameras moving parallel to the plane.
2d image projections are computed per each point and camera observing that point
using the true locations. After this step, Gaussian noise is added to the 3D coordinates
of the points (x y z) and the 6D coordinates of the cameras (x y z phi theta psi).
Then an optimization problem is formulated by defining a cost function using the 
reprojection error of the 3D points to the camera image planes.

Both Levenberg-Marquardt and Trust-Region-Reflective Least Squares are used. If it
is specified to use the second algorithm, a matrix representing the Jacobian sparsity
pattern is built to achieve a significant speedup of the optimization.

This code is written just to show the nature of a Bundle Adjustment problem and how it 
can be implemented. It meant to be used for academic purposes.

##### Usage
Just run the main script. To change the geometry of the cameras or the geometry of the
point cloud just edit the main script under the part _Pose and Point Cloud Generation_.

##### Compatibility
Written and tested on Matlab 2016a

##### Notes
If you find this code useful and you want to check my recent publications, please visit my 
ResearchGate page at this [link](https://www.researchgate.net/profile/Riccardo_Giubilato).
If you have any questions, my email address is riccardo.giubilato@gmail.com


