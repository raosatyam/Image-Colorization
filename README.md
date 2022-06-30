# Image-Colorization

The task of colourizing black and white photographs necessitates a lot of human input and hardcoding. The goal is to create an end-to-end deep learning pipeline that can automate the task of image colorization by taking a black and white image as input and producing a colourized image as output.

<a href="url"><img src="https://user-images.githubusercontent.com/96406063/176648573-ffd59db0-431c-46b0-aa52-642a661229d5.png" width="720" height = "350">

## Methodology:

•	The colorization of grayscale images can be thought of as an image-to-image translation task where we have the corresponding labels for the input grayscale image. A conditional GAN conditioned on grayscale images can be used to generate the corresponding colorized images.</br>
•	The architecture of the model consists of a conditional generator with grayscale image inputs and a random noise vector and the output of the generator are two image channels a, b in the LAB image space to be concatenated with the L channel i.e. the grayscale input image.

$ LcGAN (G, D) =Ex,y[log D(x, y)]+Ex,z[log(1 − D(x, G(x, z))],

![image](https://user-images.githubusercontent.com/96406063/176666106-8bc842d0-7b4f-45d3-9550-077087c05f5f.png)
![image](https://user-images.githubusercontent.com/96406063/176666538-cee004ee-b250-4bc1-8c79-a1e8c2c0a753.png)
![image](https://user-images.githubusercontent.com/96406063/176666829-628d48e4-e6ba-448d-b72e-e47080253caa.png)


### RGB L*A*B

RGB operates on three channels: red, green and blue. Lab is a conversion of the same information to a lightness component L*, and two color components - a* and b*. Lightness is kept separate from color, so that you can adjust one without affecting the other. "Lightness" is designed to approximate human vision, which is very sensitive to green but less to blue. If you brighten in Lab space, the result will often look more correct to the eye, color-wise. 


<a href="url"><img src="https://user-images.githubusercontent.com/96406063/176662878-a3327a91-ea30-4600-ac23-9bb934b30de7.png" width="720" height = "350">


### Generator
![image](https://user-images.githubusercontent.com/96406063/176666992-f1a02a81-8f64-42e5-8ee2-6e7962121635.png)

### Discriminator
  
### Results
  
