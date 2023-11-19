# vanhateren
Work with [Van Hateren's natural image database](https://pirsquared.org/research/vhatdb/imc/) Code works in Google Colab.

## Example

```python
import vanhateren

# Use the calibrated dataset
vh = vanhateren.VanHateren(calibrated=True)

# Get the first image (downloads automatically)
image1 = vh.image(1)

# Create num_of_patches patch_size image patches
num_of_patches = int(2.4e6)
patch_size = (3, 3)
patches = vh.patches(num_of_patches, patch_size)
```

To explicitly download more images or to download specific images,
use `VanHateren.download_image` or `VanHateren.download_images`:

```python
import vanhateren
vh = vanhateren.VanHateren(calibrated=True)
vh.download_images(range(1, 101))  # download first 100 images
```
