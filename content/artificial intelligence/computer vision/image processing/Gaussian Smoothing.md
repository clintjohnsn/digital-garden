- averaging the color values of neighboring pixels
- The **spread**, i.e. the amount of smoothing/blur is determined by the standard deviation **σ** of the Gaussian distribution used in the process. 
	- **scale selection**: selecting the required amount of scale - less important the scale, more the smoothing
	- higher the standard deviation of the distribution, less important the center pixel becomes and so more blurry the image becomes
- The image is convolved with a Gaussian **kernel**, which is a matrix representing the [[Gaussian Distribution]].
- Each pixel in the image is replaced with a weighted average of its neighboring pixels, with the weights determined by the Gaussian kernel.
- Gaussian smoothing is also **decomposable**
 ![[Convolution#Decomposable Kernels]]
- **g(a, b)** = A exp(-(a<sup>2</sup> + b<sup>2</sup> )/2σ<sup>2</sup>) = A * (exp(-(a<sup>2</sup> )/2σ<sup>2</sup>)) * (exp(-(b<sup>2</sup> )/2σ<sup>2</sup>)) 

### Why Gaussian Smoothing?
- **Anti aliasing** - blurring edges for realism
- smoothing before **sub-sampling**
- decomposable kernel (faster)
- smoothing before edge detection (for scale selection)