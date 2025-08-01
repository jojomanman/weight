# Supplement Box Image Generator - Architecture Plan

## Overview
A single HTML file application that allows users to upload CSV data, specify units, and generate a 400x400 black and white PNG image for supplement box descriptions with statistical information and plots.

## User Interface Components

1. **File Upload Section**
   - CSV file input element
   - File validation and parsing
   - Error handling for invalid files

2. **Unit Selection**
   - Dropdown with "mg" and "g" options
   - Unit conversion logic

3. **Data Processing Area**
   - Statistical calculations display
   - Visualization canvas

4. **Output Section**
   - Generated image preview
   - Download button for PNG

## Technical Implementation

### Data Flow
```mermaid
graph LR
A[User Uploads CSV] --> B[Parse CSV Data]
B --> C[Apply Unit Conversion]
C --> D[Calculate Statistics]
D --> E[Generate Plots]
E --> F[Create Composite Image]
F --> G[Display and Download]
```

### Statistical Calculations
- Mean: Σx/n
- Standard Deviation: √(Σ(x-μ)²/n)
- Sample Size: Count of data points
- Range: Max value - Min value

### Visualization Components
1. **Histogram**
   - Automatic bin sizing using Sturges' rule or similar
   - Black bars on white background
   - Properly scaled to fit in allocated space

2. **Standard Curve Plot**
   - Normal distribution curve based on calculated mean and standard deviation
   - Overlay on histogram or separate plot
   - 2 standard deviations marked

### Image Composition
- 400x400 pixel canvas
- Black and white color scheme only
- Text elements:
  - Mean value
  - Standard deviation
  - Sample size
  - Range
- Plot elements:
  - Histogram
  - Standard curve
- Clean, minimal design suitable for supplement packaging

## File Structure
Single HTML file containing:
- HTML structure
- CSS styling
- JavaScript functionality
  - CSV parsing
  - Statistical calculations
  - Canvas drawing
  - Image generation

## Technical Requirements
- Client-side only processing (no server needed)
- Compatible with Vercel deployment
- Responsive design for various screen sizes
- Error handling for edge cases