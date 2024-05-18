# Generate_Clothes_using_GAN

### Project Details:
This project aims to employ  Generative Adversarial Networks (GANs), to create realistic and diverse fashion clothing designs. By training the GAN on a diverse dataset of fashion images, encompassing various styles, patterns, and garments. Through an adversarial training process, the GAN learns to generate synthetic images that closely resemble authentic fashion designs

The GAN consists of two neural networks: a generator and a discriminator. The generator synthesizes new fashion clothing items based on random noise inputs, while the discriminator evaluates the generated images for realism, aiming to distinguish between real and fake samples. Through iterative training, both networks improve their performance, resulting in the generation of increasingly convincing fashion designs.Once trained, our GAN model can produce an infinite variety of fashion clothing items upon user request. Users can provide input parameters such as style preferences, color schemes, and garment types, influencing the generated output. The generated designs can serve as inspiration for fashion designers, retailers, and consumers, facilitating the exploration of new trends and styles.

### Libraries Used:
Numpy,Tensorflow,matplotlib,keras

## Building Generator
The generator is designed to create images from a latent vector of 100 dimensions.The generator is defined as a Sequential model, which means the layers are stacked 
in sequence .The architecture consists of several convolutional transpose layers (also known as deconvolutional layers) followed by batch normalization and rectified 
linear unit (ReLU) activation functions.

Input Layer: The generator takes a latent vector of 100 dimensions as input.
- Block 1: A convolutional transpose layer upsamples the input to a larger spatial resolution. It is followed by batch normalization and ReLU activation.
- Block 2: Another convolutional transpose layer further upsamples the feature maps. Again, batch normalization and ReLU activation are applied.
- Block 3: Similar to Block 2, this block performs additional upsampling using a convolutional transpose layer, followed by batch normalization and ReLU activation.
- Block 4: This block continues the upsampling process with another convolutional transpose layer, followed by batch normalization and ReLU activation.
- The last convolutional transpose layer aims to produce the final image. It outputs 3 channels (for RGB images)

## Building Discrimnator

The Discriminator has five convolution layers.
- The first and final Conv2D layers have Batch Normalization, since directly applying batchnorm to all layers could result in sample oscillation and model instability.
- The first four Conv2D layers use the Leaky-Relu activation with a slope of 0.2.
- Lastly, instead of a fully connected layer, the output layer has a convolution layer with a Sigmoid activation function.

## Generated Output Images:
![image](https://github.com/rjaveria/Generate_Clothes_using_GAN/assets/140335140/6a96cd53-ae64-4e68-b9a7-e50b3ed2ae53)


