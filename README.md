# Wide Gamut Test Images

This repository contains a series of wide-gamut test images. The images are prefixed with the color space of the embeded profile.

## Methodology

The primary purpose of these images is to provide simple test images for checking to see how different rendering technology is affected by non-sRGB color gamuts. For these tests, the embeded color profile keeps the same whitepoint and gamma values as the source sRGB image to reduce color and brightness variations in the output images.

## Process

These images were created via the following process:
* Create the base color(s) in Adobe Photoshop in sRGB IEC61966-2.1
* Convert the base image to the target color space:
  * Engine: "Adobe (ACE)"
  * Intent: "Absolute Colormetric"
* Create an "Overlay" image using colors from the "Target" color space.
* Create a layer mask so that differences are visible.
* Save the images as a jpeg with the "Target" color space.

## sRGB Source Specs

This is the profile information for the source color space.  These values were pulled from the [wikipedia article on sRGB](https://en.wikipedia.org/wiki/SRGB).

| Profile | xW     | yW     | xR    | yR    | xG    | yG    | xB    | yB    |
|---------|--------|--------|-------|-------|-------|-------|-------|-------|
| sRGB    | 0.3127 | 0.3290 | 0.640 | 0.330 | 0.300 | 0.600 | 0.150 | 0.060 |

The gamma value is set to 2.200

## DCI-P3 Conversion Specs

P3 prefixed images were created using a manually entered DCI-P3 profile with a D65 whitepoint. These values were pulled from the [wikipedia article on DCI-P3](https://en.wikipedia.org/wiki/DCI-P3).

| Profile    | xW     | yW     | xR    | yR    | xG    | yG    | xB    | yB    |
|------------|--------|--------|-------|-------|-------|-------|-------|-------|
| DCI-P3 D65 | 0.3127 | 0.3290 | 0.680 | 0.320 | 0.265 | 0.690 | 0.150 | 0.060 |

The gamma value is set to 2.200

## R2020 Conversion Specs

R2020 prefixed images were created using a manually entered R2020 profile with a D65 whitepoint. These values were pulled from the [wikipedia article on Rec. 2020](https://en.wikipedia.org/wiki/Rec._2020).

| Profile       | xW     | yW     | xR    | yR    | xG    | yG    | xB    | yB    |
|---------------|--------|--------|-------|-------|-------|-------|-------|-------|
| ITU-R BT.2020 | 0.3127 | 0.3290 | 0.708 | 0.292 | 0.170 | 0.797 | 0.131 | 0.046 |

The gamma value is set to 2.200
