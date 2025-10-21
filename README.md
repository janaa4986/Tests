# Catherine's Diary - Image Enhancement Project

## Overview
This project enhances the handwritten text in Catherine Ahrens Decker's travel diary PDF to maximize legibility and readability.

## Original Document
- **File:** My Travels Catherine Ahrens Decker - work file 2.pdf
- **Pages:** 44 pages
- **Size:** 17 MB
- **Source:** EPSON Scan

## Enhanced Document
- **File:** Enhanced_Catherine_Diary.pdf
- **Pages:** 22 pages (2 original pages combined per final page)
- **Size:** 26 MB
- **Processing:** Advanced image restoration techniques

## Enhancement Techniques Applied

The following advanced image processing techniques were applied to each page using ImageMagick:

### 1. **Grayscale Conversion**
   - Converted color images to grayscale for optimal text processing
   - Removes color noise and focuses on luminance information

### 2. **Normalization & Auto-leveling**
   - Normalized pixel values to use full dynamic range
   - Auto-level adjustment to optimize tonal distribution

### 3. **Contrast Enhancement**
   - Applied contrast stretching (2%x1%)
   - Brightness-contrast adjustment (+5 brightness, +15 contrast)
   - Adaptive level adjustment (10%-95% range with 1.1 gamma)

### 4. **Denoising**
   - Dual despeckle pass to remove scanning artifacts
   - Median filter (radius 1) to reduce salt-and-pepper noise
   - Overall noise reduction for cleaner text

### 5. **Sharpening**
   - Multi-pass sharpening approach:
     - Initial sharpen (0x1.5)
     - Unsharp mask (0x2+1.0+0.05) for edge enhancement
     - Adaptive sharpen (0x1.2) for final refinement
   - Enhances text edges while avoiding over-sharpening artifacts

### 6. **Detail Enhancement**
   - Enhanced filter to improve local detail
   - Preserves handwriting characteristics while improving clarity

### 7. **Page Combination**
   - Combined 2 original pages per final page (side-by-side layout)
   - Reduced document from 44 to 22 pages
   - Maintains readability while creating more compact format

## Processing Pipeline

```
Original PDF (44 pages)
    ↓
Extract pages as PNG @ 300 DPI
    ↓
Apply enhancement pipeline:
  - Grayscale conversion
  - Normalize & auto-level
  - Contrast stretching
  - Denoising (despeckle + median filter)
  - Sharpening (multi-pass)
  - Detail enhancement
  - Brightness/contrast adjustment
  - Final level adjustment
    ↓
Combine pages (2 per sheet)
    ↓
Generate final PDF (22 pages)
```

## Results

### Before & After Comparison
See `comparison_sample.png` for a visual comparison of the enhancement quality.

**Original:** Low contrast, noisy background, faded handwriting
**Enhanced:** High contrast, clean background, sharp and legible text

### Document Size Reduction
- **Original:** 44 pages → **Enhanced:** 22 pages (50% reduction)
- Better for printing and digital viewing

### Quality Improvements
- ✓ Significantly improved text legibility
- ✓ Enhanced handwriting clarity
- ✓ Reduced background noise and artifacts
- ✓ Better contrast for easier reading
- ✓ Sharper text edges
- ✓ Preserved original content authenticity

## Technical Specifications

### Tools Used
- **ImageMagick** - Advanced image processing
- **pdftoppm** - PDF to image conversion
- **Ghostscript** - PDF generation

### Processing Parameters
- **Resolution:** 300 DPI for extraction
- **Color Space:** Grayscale
- **Bit Depth:** 8-bit
- **Output Format:** PNG → PDF

## Files in Repository

1. `My Travels Catherine Ahrens Decker - work file 2.pdf` - Original scanned document
2. `Enhanced_Catherine_Diary.pdf` - Enhanced document with improved legibility
3. `comparison_sample.png` - Visual comparison of original vs enhanced
4. `Page 1 Catherine's Diary.jpg` - Sample page
5. `README.md` - This documentation

## Usage

To view the enhanced document, open `Enhanced_Catherine_Diary.pdf` in any PDF reader. The handwritten text should now be much clearer and easier to read.

## Notes

- All processing was done using intrinsic image processing tools (ImageMagick, Ghostscript)
- No external websites or Python scripts were used
- Enhancement preserves the original content without modification
- Only image quality improvements were applied
- All handwritten text and headings are preserved
