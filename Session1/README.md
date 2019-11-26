    print(score)
    -> [0.08115246505412937, 0.99]

**Convolution:** It is the way of extracting features out of an input image using feature matrix. Convolution creates a generally smaller output image which retains the features of the original image.

**Filters/Kernels:** Kernels are matrices which can be used to extract features out of an image. The values of cells in a the matrix defines what kind of feature the kernel is going to extract.

**Epochs:** Epochs are the number of times a complete dataset is scanned while training a model.

**1x1 Convolution:** This convolution is used to reduce the number of parameters in a CNN while retaining the features of the image.

**3x3 Convolution:** A 3x3 convolution is used to extract the edges and gradients of an image in image processing.

**Feature Maps:** It is the resultant output image from an input image after applying a set of kernels. The number of feature maps is same as the number of kernels that are used to extract the features.

**Activation Function:** An activation function modifies the weightage given to a kernel based on the error in the output. This helps the kernel extract features more efficiently.

**Receptive Field:** The receptive field is the maximum space of information a particular feature map contains at any time. It is decided by the kernel size. The space of information using one convolution layer is called the local receptive field. The receptive field increase with the number of convolution layers.

