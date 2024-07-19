**Corner:** Point where 2 edges meet. i.e., rapid changes of image intensity in 2 directions

- Taking gradients
![[Pasted image 20240531131234.png]]
- distribution of gradients

![[Pasted image 20240531131256.png]]

→ Classify the distribution of gradients to detect corners

- Moravec corner detector
- Harris Corner Detector
## Harris Corner Detector 
- Fitting an Ellipse to the distribution
![[Pasted image 20240531132931.png]]
- the length of the axes become the parameters
	- if both axis are small → flat region
	- if λ<sub>1</sub> >> λ<sub>2</sub> → edge region
	- if both are large → **corner** region
		- **response** function maps axis values to a number R 
			- **R** = λ<sub>1</sub> λ<sub>2</sub>  - k (λ<sub>1</sub> + λ<sub>2</sub>) <sup>2</sup>
			- where 0.04 ≤ **k** ≤ 0.06 
		- if **R** > threshold **T** → both axes are sufficiently large → Corner region
		- ![[Pasted image 20240531132753.png]]
		- ![[Pasted image 20240603123619.png]]
		- ![[Pasted image 20240603123633.png]]
- Finding axes values
- ![[Pasted image 20240531133027.png]]
- invariant to image rotation
- not scale invariant
	- Use **Harris-Laplace**
		- multiscale harris corner detection
		- scale = **Laplacian of Gaussian**, approximated by **Difference of Gaussians**
#### Non-Maximal Suppression
- The detector is likely to produce large responses not only at the exact location of the feature but also close to it
	- find the exact locations of the corners → detect the peak of each of these clusters → find local maximas
- Slide a window of size **k** over the image
	- if the pixel at the center is the maximum value within the window, label it as positive (retain it). 
	- Else label it as negative (suppress it → reduced values, or eliminate it → set to 0)

