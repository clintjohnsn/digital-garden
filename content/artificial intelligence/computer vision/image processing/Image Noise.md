### Noise
- small scale stochastic (random) fluctuations
- in computer vision, **noise** is assumed to be **normally distributed** with a mean of **0** and some standard deviation **σ**
### Scale
- size of structures of interest
- small scale structures may be noise
- when we have small **scale** structures in an image (or a series of still images), it might be noise or actual structures. if it is noise, it will vary across images.
## Signal to Noise Ratio
- **SNR** = max<sub>signal</sub>/ σ <sub>noise</sub>
- higher means (more signal per noise) so better images

## Noise Reduction
### Temporal  Averaging
-  If we have multiple still images
- averaging the images reduces the noise 
- if we average **N** images with noise of standard deviation **σ**, the noise reduces by a factor of **sqrt(N)** 
- **σ <sub>noise</sub>** = σ / sqrt(N)

### Spatial Averaging
- a.k.a. **Local Averaging**
- The idea is that the **neighbourhood** of a pixel is similar to the pixel
- replace centre pixel value by average of the **neighbourhood** pixel value including the centre pixel
- The higher the neighbourhood, more the noise goes down BUT the picture becomes more blurry/loss of **sharpness**/loss of spatial information/ loss of small scale structures
	- this happens because the principle spatial similarity does not hold true for edges
- a type of [[Convolution]]