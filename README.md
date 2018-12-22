# Wide Gamut Test Images

This repository contains a series of wide-gamut test images. The images are prefixed with the color space of the embedded profile.

## Methodology

The primary purpose of these images is to provide simple test images for checking to see how different rendering platforms treat images with non-sRGB color gamuts.

The first test is a "RGB to GBR" test. This determines if a target platform uses or discards color profiles on an image. If the target platform doesn't honor color profiles, the remaining tests are meaningless and the watermarks will show in all of the other test cases.

The second series of tests show _which_ gamuts the target platform is capable of displaying. Watermarks will appear when the image is viewed on a platform that is capable of rendering wide gamut content that is larger than the gamut of the source color space. For these tests, the embedded color profiles keep the same whitepoint and gamma values as the source image to reduce color and brightness variations.

## RGB to GBR Rendering Test

This test image was created by assigning a custom profile that rotates the RGB primary color points from the original sRGB color profile. Red -> Green, Green -> Blue, Blue -> Red. If the words and colors are aligned, then the color profile was read and rendered correctly, if not, then the device discarded or ignored the color profile and the remaining tests are meaningless.

| Profile | W<sub>x</sub>| W<sub>y</sub>| R<sub>x</sub>| R<sub>y</sub>| G<sub>x</sub>| G<sub>y</sub>| B<sub>x</sub>| B<sub>y</sub> |
|------------|--------|--------|-------|-------|-------|-------|-------|-------|
| RGB to GBR | 0.3127 | 0.3290 | 0.150 | 0.060 | 0.640 | 0.330 | 0.300 | 0.600 |

The gamma value is set to 2.200

### JPG
* [rgb-to-gbr-test.jpg](rgb-to-gbr-test.jpg)

### PNG
* [rgb-to-gbr-test.png](rgb-to-gbr-test.png)

## Wide Gamut Test Image Creation Process

These images were created via the following process:
* Configure Photoshop to Preserve Color Profiles and to always ask when opening, pasting, or if there is a missing profile.
* Create a solid color or gradient in the "Target" color space (P3 or R2020)
* Copy the solid color or gradient into a document that's in sRGB space and convert the colors to the the "Source" space (sRGB) using the "Preserve Color Appearance" option.
  * Engine: "Adobe (ACE)"
  * Intent: "Absolute Colormetric"
* Copy the the source version back to the original image using the "Preserve Color Appearance" option.
* Create a layer mask so that differences are visible.
* Save the images as a jpeg with the "Target" color space.

## sRGB Source Specs

This is the profile information for the source color space.  These values were pulled from the [wikipedia article on sRGB](https://en.wikipedia.org/wiki/SRGB).

| Profile | W<sub>x</sub>| W<sub>y</sub>| R<sub>x</sub>| R<sub>y</sub>| G<sub>x</sub>| G<sub>y</sub>| B<sub>x</sub>| B<sub>y</sub> |
|---------|--------|--------|-------|-------|-------|-------|-------|-------|
| sRGB    | 0.3127 | 0.3290 | 0.640 | 0.330 | 0.300 | 0.600 | 0.150 | 0.060 |

The gamma value is set to 2.200

## DCI-P3

P3 prefixed images were created using a manually entered DCI-P3 profile with a D65 whitepoint. These values were pulled from the [wikipedia article on DCI-P3](https://en.wikipedia.org/wiki/DCI-P3).

| Profile | W<sub>x</sub>| W<sub>y</sub>| R<sub>x</sub>| R<sub>y</sub>| G<sub>x</sub>| G<sub>y</sub>| B<sub>x</sub>| B<sub>y</sub> |
|------------|--------|--------|-------|-------|-------|-------|-------|-------|
| DCI-P3 D65 | 0.3127 | 0.3290 | 0.680 | 0.320 | 0.265 | 0.690 | 0.150 | 0.060 |

The gamma value is set to 2.200

### JPG's
* [P3-sRGB-red.jpg](P3-sRGB-red.jpg)
* [P3-sRGB-green.jpg](P3-sRGB-green.jpg)
* [P3-sRGB-blue.jpg](P3-sRGB-blue.jpg)
* [P3-sRGB-color-ring.jpg](P3-sRGB-color-ring.jpg)
* [P3-sRGB-color-bars.jpg](P3-sRGB-color-bars.jpg)

### PNG's
* [P3-sRGB-red.png](P3-sRGB-red.png)
* [P3-sRGB-green.png](P3-sRGB-green.png)
* [P3-sRGB-blue.png](P3-sRGB-blue.png)
* [P3-sRGB-color-ring.png](P3-sRGB-color-ring.png)
* [P3-sRGB-color-bars.png](P3-sRGB-color-bars.png)

## Rec. 2020

R2020 prefixed images were created using a manually entered R2020 profile with a D65 whitepoint. These values were pulled from the [wikipedia article on Rec. 2020](https://en.wikipedia.org/wiki/Rec._2020).

| Profile | W<sub>x</sub>| W<sub>y</sub>| R<sub>x</sub>| R<sub>y</sub>| G<sub>x</sub>| G<sub>y</sub>| B<sub>x</sub>| B<sub>y</sub> |
|---------------|--------|--------|-------|-------|-------|-------|-------|-------|
| ITU-R BT.2020 | 0.3127 | 0.3290 | 0.708 | 0.292 | 0.170 | 0.797 | 0.131 | 0.046 |

The gamma value is set to 2.200

### Rec. 2020 vs sRGB
#### JPG's
* [R2020-sRGB-red.jpg](R2020-sRGB-red.jpg)
* [R2020-sRGB-green.jpg](R2020-sRGB-green.jpg)
* [R2020-sRGB-blue.jpg](R2020-sRGB-blue.jpg)
* [R2020-sRGB-color-ring.jpg](R2020-sRGB-color-ring.jpg)
* [R2020-sRGB-color-bars.jpg](R2020-sRGB-color-bars.jpg)

#### PNG's
* [R2020-sRGB-red.png](R2020-sRGB-red.png)
* [R2020-sRGB-green.png](R2020-sRGB-green.png)
* [R2020-sRGB-blue.png](R2020-sRGB-blue.png)
* [R2020-sRGB-color-ring.png](R2020-sRGB-color-ring.png)
* [R2020-sRGB-color-bars.png](R2020-sRGB-color-bars.png)

### Rec. 2020 vs P3
#### JPG's
* [R2020-P3-red.jpg](R2020-P3-red.jpg)
* [R2020-P3-green.jpg](R2020-P3-green.jpg)
* [R2020-P3-blue.jpg](R2020-P3-blue.jpg)
* [R2020-P3-color-ring.jpg](R2020-P3-color-ring.jpg)
* [R2020-P3-color-bars.jpg](R2020-P3-color-bars.jpg)

#### PNG's
* [R2020-P3-red.png](R2020-P3-red.png)
* [R2020-P3-green.png](R2020-P3-green.png)
* [R2020-P3-blue.png](R2020-P3-blue.png)
* [R2020-P3-color-ring.png](R2020-P3-color-ring.png)
* [R2020-P3-color-bars.png](R2020-P3-color-bars.png)
