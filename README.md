# Coccolith-analysis

In my research I collected 4D datasets consisting of a 2D image (real space) where each pixel has a 2D image (diffraction space) associated to it. The real space image consists of crystals in different orientations while the diffraction space image consists of diffraction peaks and is important to determine the crystallographic orientation. In the lab we have a code that processes the diffraction images and saves important values in a .JSON file. I will use this dataset for this python project. 
The project consists of two main parts:

Part 1: Segmentation of the real space image
We input a .JSON file containing a list of peaks for each pixel of the real space image.
1.	Transform the JSON file into a 2D matrix where each entry contains the list of peaks for the specific pixel.
2.	Select neighboring regions in which the list of peaks in the .JSON file are the same within a margin of error and assign to a segment.
3.	Average the peaks belonging to a segment and use them for orientation analysis.
4.	Plot the 2D real space image color coded where each segment of the image corresponds to a specific color.

Part 2: Representation of the orientation of the segments using a stereogram
Stereograms are a useful tool for crystallography since they allow to represent a 3D orientation of a crystal in 2D. The main idea behind it, is to project the vectors representing the x, y, z axis of a crystal on top of a stereogram that is a grid containing information on the orientation angles of the vectors.  We will implement the following functions:
1.	Initialize the stereogram map. The stereogram consists in longitudinal and latitudinal 3D circles projected in 2D. We will define the circles and project them in 2D.
2.	Projection of the axis. We will have a function that projects a vector from 3D to 2D
3.	Trace of a vector. This is the projection of the plane perpendicular to a given vector

In the end we will connect part 1 and 2 in such a way that the segments will be color coded based on their orientation which we obtain with the stereogram.
