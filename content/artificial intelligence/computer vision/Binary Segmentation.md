### Thresholding based
- For a greyscale image, it often suffices to apply a threshold value to the image function to segment the image
- **b**(x,y) = (**g**(x,y) <*T*)
	- *T* is the threshold greyscale value
	- **g**(x,y) is the image function
	- **b**(x,y) is a binary image
		- image with 2 values - 1s and 0s
		- foreground and background will be shaded with 1s and 0s respectively
- need to choose threshold with care
	- **automatic threshold selection** 
		- several threshold selection algorithms
		- one method is to use image histogram
			- Threshold placed where rate of change of segmented area is smallest
### Adaptive Thresholding
- where a simple **global** threshold value is not good enough, use **Adaptive thresholding** (**local** thresholds)
- thresholds are localized
- an estimate of background shading can be used 
- perform [[Image smoothing]] using something like a  [[Gaussian Smoothing]], and then subtract the resulting estimate of background variance from the original image, giving a background corrected image. Then perform thresholding over this.
