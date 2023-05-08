# A PyTorch implementation of C-FCN 

This is my implementation of C-FCN, a low power CNN for cloud segmentation, proposed in "Low-power neural networks for semantic segmentation of satellite images" (Balh et. al, [2019](https://openaccess.thecvf.com/content_ICCVW_2019/papers/LPCV/Bahl_Low-Power_Neural_Networks_for_Semantic_Segmentation_of_Satellite_Images_ICCVW_2019_paper.pdf)) 

Apart from implemented the orignal architecture, I also add the option to change to final layer in an attempt to improve accuracy (evaluation in progress). These are the available options: 

+ Bilinear Upscaling (original)
+ 2D Transpose Convolution (scale factor: 4)
+ 2x 2D Transpose Convolution (scale factor: 2)

Skipped connection is also implemented

To change configuration:

<pre>model = C_FCN(input_channel, output_channel, 
              last_layer, # "BI" for bilinear upscaling
                          # "TC" for transpose convolution
                          # "DT" for double transpose convolution 
              skipped_connection # boolean)</pre>

