# Depth Estimation of Martian Surface using images from ISRO's MARS Color Camera.

<h2>Published</h2>

**Published in: 2021 2nd Global Conference for Advancement in Technology (GCAT) - [Paper link](https://ieeexplore.ieee.org/document/9587677)<br>
Date of Conference:** 1-3 Oct. 2021<br>
**Date Added to IEEE Xplore:** 13 November 2021<br>
**ISBN Information:<br>**
Electronic ISBN:978-1-6654-1836-2<br>
Print on Demand(PoD) ISBN:978-1-6654-3070-8<br>
**INSPEC Accession Number:** 21297225<br>
**DOI:** 10.1109/GCAT52182.2021.9587677<br>
**Publisher:** IEEE<br>
**Conference Location:** Bangalore, India<br>

<h2>Authors</h2>

- [Akash Khamkar](https://github.com/AkashKhamkar)
- [Arjun Pukale](https://github.com/ArjunPukale)
- [Prathamesh Joshi](https://github.com/prathamesh1499)

<h2>Abstarct</h2>
Depth estimation from satellite images is a fundamental task when studying the terrain of a celestial body. Existing solutions for depth estimation often use datasets that include either images of an indoor scene or images related to (self-driving). This paper presents a Pix2pix type of neural network for computing the depth of the Martian surface using the images captured by ISRO’s Mars Orbiter. In this paper, we have implemented Pix2Pix (Generator Discriminator) architecture using two different loss functions- LSGAN and Vanilla loss functions and then compared their results to select a better loss function for computing accurate depth maps.<br><br>
Currently, the Indian Space Research Organization (ISRO) is carrying out various research projects regarding the planet Mars. Earlier, it deployed Mars orbiter in the year 2013 for collecting information which can be further used for conducting even more in-depth research about the planet’s topography, temperature, atmosphere, etc.<br><br>

One such research area that ISRO is currently focusing on is estimating the depths of various valleys, canyon systems of the Martian planet. As per the current scenario, one such method for estimating depths is using Lidar technology.

We proposed a method where we use Generative Adversarial Networks to estimate such Depth Maps using just a single input image, without using hardwares like sterio, lidar, etc. This Depth Map can be further used for creating 3D models or simulations of the surface for researching and further planning of future missions.

<h2>Data Collection</h2>
For this project currently there exists no specific dataset, which consists of both the satellite images and the depth maps, hence we created our own dataset for this project.
The dataset we created consists of two type of images -

1. Satellite images which were taken from ISRO’s Mars Orbiter in different lighting conditions.
2. Depth image obtained from NASA’s MOLA map.

<h2>Data Processing</h2>

1. We gathered 1:1 identical pair of images from Isro satellite images and Nasa's Mola Depth Map respectively, along Valles Marineris canyon system at the map scale of 53km .
2. A total of 38 images were collected which were captured by MOM at different intervals of time in its orbits.
3. Each image was augmented to a set of 10 images thus reaching a total count of 380 images.
4. Different augmentation techniques were used such as :
   - Resize
   - Rotate
   - Shift Scale
   - Center Crop
   - Horizontal flip
   - Vertical flip
   - Blur
   - Brightness
   - Contrasts
   - Hue Saturation
5. These images were randomly partitioned into training  & testing  .
6. Each Training Image is of size 256x256.

<h2>Sample Pair Image</h2>

![image](https://user-images.githubusercontent.com/34622497/154837542-54fbdea5-266a-468d-a4a2-245bc82ae23b.png)

<h2> Model Used</h2>

We have used [Pix2Pix](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix) model to solve this Task.
![image](https://user-images.githubusercontent.com/34622497/154837781-11eb10ed-b56a-4511-bd06-41938ce442ca.png)<br>
We have tested this model with two loss functions: Vanilla Gan Loss and Lsgan Loss.

<h2>Results</h2>

![image](https://user-images.githubusercontent.com/34622497/154837905-35a66a2d-8113-444f-97e6-2d7e278781fc.png)

<h3>Loss Function vs Performance Metrics:</h3>

![image](https://user-images.githubusercontent.com/34622497/154838185-30e12f2d-8c5a-413b-bd6c-48998c5a022b.png)

<h3>Performance Metric Distribution:</h3>

![image](https://user-images.githubusercontent.com/34622497/154838195-286acc52-fbc7-4f05-bbd1-05ff327411ee.png)

<h2>References</h2>

```
@inproceedings{isola2017image,
  title={Image-to-Image Translation with Conditional Adversarial Networks},
  author={Isola, Phillip and Zhu, Jun-Yan and Zhou, Tinghui and Efros, Alexei A},
  booktitle={Computer Vision and Pattern Recognition (CVPR), 2017 IEEE Conference on},
  year={2017}
}
```

