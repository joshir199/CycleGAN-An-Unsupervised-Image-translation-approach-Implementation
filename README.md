# Implementation CycleGAN An Unsupervised Image to Image translation approach
Understanding and Implementing the CycleGAN approach for Unsupervised Image to Image translation for Style transfer and other usecases like modifying art to new style.

An unsupervised learning approach has been used to address the lack of paired training data in case of Image to Image translation. Obtaining huge amount of such paired image data can be challenging and expensive, limiting the applicability of other supervised methods.

CycleGAN has had a significant impact on the field of computer vision and image processing. It has opened up new possibilities for creating artistic and stylized images, domain adaptation, and data augmentation without the need for paired training data. The idea of cycle-consistency has been widely adopted in subsequent research.

Research Paper refered : https://arxiv.org/abs/1703.10593

For theoretical explanation and more similar papers, refer here: https://github.com/joshir199/Revisiting-famous-Deep-Learning-research-papers

# The Setup
The model contains two mapping functions G : X -> Y and F : Y -> X, and associated adversarial discriminators Dy and Dx. Dy encourages G to translate X into outputs indistinguishable from domain Y , and vice versa for Dx and F.


-----------------------------------------------
Dataset used for this Cycle-GAN model training :

Description: The CMP Facade Database data (30MB) has been used for this training task. Dataset contains a total of 400 images of real houses as well as its architectural drawing. Each original image is of size 256 x 512 containing two 256 x 256 images.

Dataset source: http://efrosgans.eecs.berkeley.edu/pix2pix/datasets/facades.tar.gz

![](https://github.com/joshir199/CycleGAN-An-Unsupervised-Image-translation-approach-Implementation/blob/main/image_from_dataset.png)

********************************************
# Training process

EPOCHS (=10) has been kept small as it needs very high computation power. The generated images will have much lower quality. Also, BATCH_SIZE = 1 is kept as U-NET generator model learning better with single Batch size.

![](https://github.com/joshir199/CycleGAN-An-Unsupervised-Image-translation-approach-Implementation/blob/main/model_training_generated_images.gif)

->  Training result showing how generator learns to generate better images with style transfer

********************************************
# Test results

![](https://github.com/joshir199/CycleGAN-An-Unsupervised-Image-translation-approach-Implementation/blob/main/output/drawing_image_to_house.png)

**********************************
# Applications:
The effectiveness of CycleGAN can be seen on various image-to-image translation tasks, such as converting photographs into the style of famous paintings, transforming horse images into zebra images, and changing the season in photographs.
