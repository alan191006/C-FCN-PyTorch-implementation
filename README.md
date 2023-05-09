# C-FCN PyTorch Implementation

This is a PyTorch implementation of C-FCN, a low power convolutional neural network for cloud segmentation in satellite images, as proposed in "Low-power neural networks for semantic segmentation of satellite images" (Balh et al., [2019](https://openaccess.thecvf.com/content_ICCVW_2019/papers/LPCV/Bahl_Low-Power_Neural_Networks_for_Semantic_Segmentation_of_Satellite_Images_ICCVW_2019_paper.pdf)).

In addition to implementing the original C-FCN architecture, this implementation includes an option to change the final layer to potentially improve accuracy. The available options for the final layer are:

- Bilinear Upscaling (original)
- 2D Transpose Convolution (scale factor: 4)
- 2x 2D Transpose Convolution (scale factor: 2)

This implementation also includes a skipped connection.

## Usage

To use this implementation, simply create an instance of the `C_FCN` class with the appropriate parameters:



<pre>model = C_FCN(input_channel, output_channel, last_layer, skipped_connection)</pre>


- `input_channel` is the number of channels in the input image
- `output_channel` is the number of output classes
- `last_layer` specifies the type of final layer to use: `"BI"` for bilinear upscaling, `"TC"` for transpose convolution, or `"DT"` for double transpose convolution
- `skipped_connection` is a boolean indicating whether to use a skipped connection in the network.

## License

This implementation is licensed under the MIT License.

## Acknowledgements

This implementation is based on the original paper by Balh et al. (2019).
