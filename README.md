# Image-Colorization

The task of colourizing black and white photographs necessitates a lot of human input and hardcoding. The goal is to create an end-to-end deep learning pipeline that can automate the task of image colorization by taking a black and white image as input and producing a colourized image as output.

<a href="url"><img src="https://user-images.githubusercontent.com/96406063/176648573-ffd59db0-431c-46b0-aa52-642a661229d5.png" width="720" height = "350">

## Methodology:

•	The colorization of grayscale images can be thought of as an image-to-image translation task where we have the corresponding labels for the input grayscale image. A conditional GAN conditioned on grayscale images can be used to generate the corresponding colorized images.</br>
•	The architecture of the model consists of a conditional generator with grayscale image inputs and a random noise vector and the output of the generator are two image channels a, b in the LAB image space to be concatenated with the L channel i.e. the grayscale input image.

<a href="url"><img src="https://user-images.githubusercontent.com/96406063/176681673-337b10ab-ac3d-4552-9db5-f2d003ce0200.png" width="720" height = "35">
  <a href="url"><img src="https://user-images.githubusercontent.com/96406063/176681474-04b8e936-8095-4260-a4b4-e4d53f9047d7.png" width="720" height = "35">
<a href="url"><img src="https://user-images.githubusercontent.com/96406063/176681259-7b140bc9-9bc8-4d4c-bfce-5e5c47ede77a.png" width="720" height = "35">

### RGB L*A*B

RGB operates on three channels: red, green and blue. Lab is a conversion of the same information to a lightness component L*, and two color components - a* and b*. Lightness is kept separate from color, so that you can adjust one without affecting the other. "Lightness" is designed to approximate human vision, which is very sensitive to green but less to blue. If you brighten in Lab space, the result will often look more correct to the eye, color-wise. 

<a href="url"><img src="https://user-images.githubusercontent.com/96406063/176662878-a3327a91-ea30-4600-ac23-9bb934b30de7.png" width="720" height = "350">


### Generator

### Discriminator
  
### Results

  ![image](https://user-images.githubusercontent.com/96406063/176685572-d9e0a967-2709-49e6-80e0-de750f8b22a9.png)
  
  
  
