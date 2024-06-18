# avatar-generation-using-python
This script transforms an input image into a cartoon-like avatar using image processing techniques provided by OpenCV and PIL (Python Imaging Library).

## How It Works

1. **Read the Image:**
   The script starts by reading the input image using OpenCV's `imread` function.

2. **Convert to Grayscale:**
   The image is converted to grayscale with `cvtColor` to simplify the edge detection process.

3. **Apply Median Blur:**
   A median blur is applied to reduce noise in the grayscale image, making the edge detection more accurate.

4. **Edge Detection:**
   Edges are detected using adaptive thresholding. This creates a binary image where the edges are highlighted.

5. **Bilateral Filter:**
   A bilateral filter is applied to the original image to smooth colors while preserving edges. This filter helps achieve the cartoonish look.

6. **Combine Edges and Smoothed Image:**
   The edge mask is combined with the smoothed image using a bitwise AND operation, resulting in an image with clear edges and smooth colors.

7. **Save the Output:**
   The final cartoonized image is saved to the specified output path using `imwrite`.

## Usage

- Place your input image (e.g., `input_image.jpg`) in the same directory as the script.
- Run the script, and the output image (`output_avatar.jpg`) will be created in the same directory.

## Example

```python
cartoonize_image('input_image.jpg', 'output_avatar.jpg')
```

This function reads the specified input image, processes it to create a cartoon effect, and saves the result as the specified output image.

Adjust the parameters in the script to experiment with different effects and achieve the desired cartoon look.
