# Project: Art Creation using Neural Stye Transfer
Coded in Google Colab, this project features Neural Style Transfer which is an optimization technique that merges two images, namely: a "content" image (C) and a "style" image (S), to create a "generated" image (G). The generated image G combines the "content" of the image C with the "style" of image S. 

1. A pre-trained CNN is used to extract the feature maps from the content and style images. The pre-trained CNN is the VGG network from the original NST paper published by the Visual Geometry Group at University of Oxford in 2014. Specifically, VGG-19 is used, which is a a 19-layer version of the VGG network. This model has already been trained on the very large ImageNet database, and has learned to recognize a variety of low level features (at the shallower layers) and high level features (at the deeper layers). Typically, the feature maps are extracted from intermediate layers of the network, where the network has learned to represent increasingly complex features.

2. The content and style losses are defined. The content loss measures the difference between the feature maps of the content image and the generated image, while the style loss measures the difference between the feature maps of the style image and the generated image. The content loss ensures that the generated image preserves the structure and details of the content image, while the style loss ensures that the generated image has the texture and patterns of the style image.

3. The total loss is defined as a weighted sum of the content loss and the style loss, where the weights determine the balance between preserving content and transferring style.

4. The total loss is minimized using gradient descent to generate a new image that balances the content and style of the two input images. This new image is the output of the style transfer process.
