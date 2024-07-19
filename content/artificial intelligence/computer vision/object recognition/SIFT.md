> a.k.a. Scale Invariant Feature Transform

Local Feature matching invariant to
- scale
- orientation/rotation
- illumination/brightness
- occlusion
- noise
- small changes in viewpoint

### Keypoint Localization

> See [[Edge Detection#Laplacian of Gaussian Edge Detector]]

![[Pasted image 20240531201910.png]]

- increasing **σ** (scale parameter)
- ![[Pasted image 20240531203304.png]]
- for each blob, as we increase **σ**, a peak will emerge and then fade away
- apply the **σ**-Normalized Laplacian of the Gaussian (**NLoG**) using multiple values of **σ**
- at some scale, the output will attain a peak
- characteristic scales (**σ**) ∝ the size of the blobs
- ![[Pasted image 20240531203451.png]]
- Selection of **σ**:
	- **σ**<sub>k</sub> = σ<sub>0</sub>s<sup>k</sup>, k = 0,1,2,3…
	- s = constant multiplier
	- σ<sub>0</sub> = initial scale
- Fast approximation → **DoG**
	- **DoG** = (s-1) **NLoG**

>see [[Edge Detection#Difference of Gaussians Edge Detector]]

- detect local maximas obtained
![[Pasted image 20240531205904.png]]

- **Non maximal suppression**: Run a  NxNxN grid over the stack, if the absolute value of center pixel is significantly larger than the absolute values of its neighbors in its scale and its neighbouring scales, it is declared to be an extremum.

> See [[Corner Detection#Non-Maximal Suppression]]

- use some contrast thresholding to remove weak extrema

### Orientation invariant Region Selection
- consider a square window of pixels in the blob
- get image gradient directions
- **principal orientation**: most common gradient direction
- ![[Pasted image 20240601104818.png]]

### SIFT Descriptors
- calculate gradient orientation histogram of each of the four quadrants of the grid and concatenate them → normalized histogram = SIFT descriptor
- histograms have 8 directions
- descriptor = 128 elements
- Comparing SIFT descriptors
	- [[L2 Norm]]
		- smaller value = better match
	- Normalized Correlation
		- ![[Pasted image 20240601105442.png]]
			- perfect match when **d**(H<sub>1</sub>,H<sub>2</sub>) = 1
	- Intersection
		- ![[Pasted image 20240601105805.png]]
		- larger value = better match

### Applications
- [[Object Recognition]]
- Panorama Stitching
- Auto Collages

### Limitations
- 3D objects
- different viewpoints, angles