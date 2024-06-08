# KDE-test
This code is the implementation of the research paper: Statistical change detection for multi-dimensional data.  Xiuyao Song, Mingxi Wu, Christopher Jermaine, and Sanjay Ranka. 2007 In Proceedings of the 13th ACM SIGKDD international conference on Knowledge discovery and data mining (KDD ’07). Association for Computing Machinery, New York, NY, USA, 667–676.  

Kernel density estimation test (KDE test) is proposed in the research paper for change detection in multi-dimensional data. I have done implementation on the MNIST dataset. MNIST images are used because it is easy and fast to examine and visualize the implementation of this research paper using these images. The implementation is done using python. 

Any single image in the MNIST is treated as dataset of interest. I have then detected the change by two ways. First being comparing the image with entirely different image and second being adding some noise (3-4 %) to the same image and comparing this noisy image with the original image to detect the change. In both the cases, code is giving expected results. The code can detect the change with noise as low as 2% in some cases.  Of course this is not the ideal method to detect small change in image, but it just validates the implementation.

Since the dataset used is an image, I have done a small adjustment. Splitting an image (dataset= S) into two datasets S1 and S2 doesn’t make sense, because then image will be split. Hence, in this code I have considered S = S1 = S2 which kind of makes sense because by doing so, S1 and S2 are most likely to represent the distribution of S. The dataset S’ is the noisy image or entirely different image from MNIST.     
Same code can be used for other non-image (numerical) datasets. In that case, we have to split the original dataset S into two datasets S1 and S2 . Everything will be same except data pre-processing.
 
