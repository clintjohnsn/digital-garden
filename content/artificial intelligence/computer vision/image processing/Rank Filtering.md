- Similar to [[Convolution]]
- Take values under the kernel/mask/filter window, and order them on **intensity**
	- pick
		- First: minimum/erosion
		- Last: maximum/dilation
		- Middle value: **median filtering** 
		- Other: e.g. 7th of 9 in a 3x3 window

## Median Filtering
- better than **mean filtering** or **spatial averaging** ( see [[Image Noise#Spatial Averaging]])
	- removes noise and smoothens while keeping edges
	- especially useful with *salt and pepper* noise
