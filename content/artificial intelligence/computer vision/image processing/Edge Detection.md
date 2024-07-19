- An **edge** is a place of rapid change in the image intensity function (or grey-level function), which manifests as boundaries between physically distinct regions.
	- i.e. a peak in the derivative of the image function
![[Pasted image 20240423140805.png]]
## Convolution based Edge Detection>

>see [[Convolution]]

- Edge detection is same as differentiation a.k.a. **derivative filter**
- -![[Pasted image 20240423190223.png]]
-  gradient direction is perpendicular to the edge
#### Derivative of Gaussian convolution kernel
> see [[Gaussian Distribution]]

- For **noisy** images - 
	- **scale selection** is important
		- edges may be noise
		- Location of edges at coarse scale can direct the search for finer-scale edges
		- edges can persist across scales, allows fusion across scales 
	- Perform [[Image smoothing]] before derivative filter to reduce effect of noise
![[Pasted image 20240423141211.png]]
![[Pasted image 20240423141227.png]]
- Derivative of Gaussian filter in 2 dimensions, along x
![[Pasted image 20240423205739.png]]
- derivatives can be along x and y directions (2 filters) → requires atleast 2 convolutions
- allows selection of scale of edge detection 
	- through **σ**
![[Pasted image 20240531202240.png]]
### Kernels

#### Prewitt Kernel
- vertical edges, detecting edges across x direction, smooths along y direction
	- -1 0 1
	- -1 0 1
	- -1 0 1
- horizontal edges, detecting edges across y direction, smooths along x direction
	- -1 -1 -1
	- 0  0  0
	- 1  1   1
#### Sobel Kernel
- vertical edges, detecting edges in x direction, weighted smoothing along y direction 
	- -1 0 1
	- -2 0 2
	- -1 0 1
- horizontal edges, detecting edges in y direction, weighted smoothing along x direction
	- -1 -2 -1
	-  0  0  0
	-  1  2  1
- 2 filters: Derivative images **I’<sub>x</sub>** and **I’ <sub>y</sub>**  
![[Pasted image 20240531033422.png]]
### Laplacian of Gaussian Edge Detector

> a.k.a. Marr–Hildreth Edge Detector
>  a.k.a. Mexican hat wavelet

- second derivative of gaussian kernel
- ![[Pasted image 20240531034008.png]]
- 2nd Derivative of Gaussian filter in 2 dimensions
- ![[Pasted image 20240423212138.png]]
- detect zero crossings → where the 2nd derivative crosses zero → indicates an edge
- convolution kernel has a negative center and a  positive surrounding
- again, **scale selection** is done through **σ**
- **isotropic** response
	- one filter (all directions) 
		- no edge direction 
	- indirect edge magnitude
- kernel examples
```
 2  -1  2 
-1  -4 -1  
 2  -1  2

1   1   1
1  -8   1
1   1   1

``` 
![[Pasted image 20240423212205.png]]
![[Pasted image 20240531202130.png]]
###  Canny Edge Detector
- best attributes of both the gradient operator and the Laplacian operator
- Multi stage algorithm
	1. [[Gaussian Smoothing]] to select scale and smoothen
	2. edge detection
		- convolve image intensity function with **derivative of Gaussian** (Sobel operator) 
		- Edge magnitude and direction detected
	3. Compute **Laplacian of Gaussian** along the Gradient Direction at each pixel
		- zero crossings → edge location
		- less effected by pixels that are unrelated to the edge
	4. **thinning**: suppress non maxima of derivative
		- non maxima derivatives across an edge
		- **sub pixel precision**: detect precise edge locations
	5. Track using **hysteresis thresholds**
		- Finalize the detection of edges by suppressing all the other edges that are weak and not connected to strong edges.
		- declare each pixel as being an edge or not
		- single threshold:  if the edge magnitude is less than some value T it is not an edge
		- ![[Pasted image 20240531033843.png]]
### Difference of Gaussians Edge Detector
- a fast approximation of the **Laplacian of Gaussians**
- subtraction of one Gaussian-Blurred ([[Gaussian Smoothing]]) version of an image from another, less blurred image
- for scales of gaussians sσ and σ →
- ![[Pasted image 20240531205140.png]]
- DoG = (s-1) NLoG


### Edge illusions 
Cannot be detected using edge detectors
#### Herring Illusion
![[Pasted image 20240531135358.png]]
horizontal lines are actually parallel

#### Cafe Wall Illusion
![[Pasted image 20240531135447.png]]
horizontal lines are actually parallel