# Handwritten Text Image Enhancement

This repository contains an enhanced version of Catherine's Diary page using advanced image processing techniques.

## Original Image
- **File**: `Page 1 Catherine's Diary.jpg`
- **Resolution**: 589x767 pixels at 120 DPI
- **Format**: JPEG color image
- **Issues**: Low contrast, moderate noise, suboptimal for text readability

## Enhanced Versions

### 1. Standard Enhanced Version
**File**: `Page 1 Catherine's Diary Enhanced.jpg`
- **Resolution**: 589x767 pixels at 300 DPI
- **Size**: 190 KB
- **Techniques Applied**:
  - Grayscale conversion for optimal text contrast
  - Dual despeckle for noise reduction
  - Contrast stretching (2%x1%)
  - Normalization to full dynamic range
  - Adaptive sharpening (0x1.5)
  - Unsharp mask (0x2+1+0.05) for text edge enhancement
  - Quality preservation at 95%

### 2. Advanced Enhanced Version
**File**: `Page 1 Catherine's Diary Advanced Enhanced.jpg`
- **Resolution**: 589x767 pixels at 300 DPI
- **Size**: 13 KB
- **Techniques Applied**:
  - Grayscale conversion
  - Gaussian morphological convolution for smoothing
  - Local Adaptive Thresholding (LAT) 15x15+10% for optimal text/background separation
  - Contrast stretching (1%x1%)
  - Sigmoidal contrast enhancement (10x50%) for non-linear contrast boost
  - Adaptive sharpening (0x2)
  - Unsharp mask (2x1+1+0.05) for crisp text edges
  - High quality output at 98%

### 3. Super-Resolution Version
**File**: `Page 1 Catherine's Diary Super-Resolution.jpg`
- **Resolution**: 1178x1534 pixels at 600 DPI (2x upscaling)
- **Size**: 676 KB
- **Techniques Applied**:
  - Grayscale conversion
  - Despeckle noise reduction
  - Double enhancement pass
  - 200% resolution scaling using advanced interpolation
  - Heavy unsharp mask (0x5+0.5+0) for super-sharp text
  - Contrast stretching (2%x2%)
  - Auto-leveling for optimal tonal distribution
  - Adaptive sharpening (0x3)
  - Maximum quality preservation at 98%

## Enhancement Methodology

All enhancements were performed using ImageMagick 6.9.12-98, leveraging:

1. **Denoising**: Despeckle and Gaussian morphology to reduce artifacts
2. **Contrast Adjustment**: Multiple techniques including normalization, contrast-stretch, sigmoidal-contrast, and auto-level
3. **Sharpening**: Adaptive sharpening and unsharp masking for text edge enhancement
4. **Super-Resolution**: 2x upscaling with advanced interpolation algorithms
5. **Local Adaptive Processing**: LAT for intelligent text/background separation

## Recommended Version

- **For general readability**: Use `Page 1 Catherine's Diary Enhanced.jpg`
- **For maximum text clarity with strong contrast**: Use `Page 1 Catherine's Diary Advanced Enhanced.jpg`
- **For zooming and detailed inspection**: Use `Page 1 Catherine's Diary Super-Resolution.jpg`

## Technical Details

All processing was performed without Python, using only ImageMagick's built-in capabilities:
- No external services or websites used
- Pure image processing algorithms
- Optimized for handwriting legibility
- Preservation of original document characteristics while maximizing readability
