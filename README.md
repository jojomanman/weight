# Supplement Box Image Generator

A single HTML file application that allows users to upload CSV data with weight measurements, specify units, and generate a 400x400 black and white PNG image for supplement box descriptions.

## Features

- Upload CSV files with weight measurements
- Select units (mg or g)
- Calculate statistics (mean, standard deviation, sample size, range)
- Generate histogram visualization
- Create a supplement box image with all calculated information
- Download the generated image as a PNG file

## How to Use

1. Upload a CSV file containing weight measurements (one value per line)
2. Select the appropriate unit (mg or g)
3. Click "Generate Supplement Box Image"
4. View the calculated statistics and visualization
5. Download the generated 400x400 black and white PNG image for your supplement box

## Deployment to Vercel

1. Create a new project on [Vercel](https://vercel.com)
2. Connect your GitHub repository or upload the `index.html` file directly
3. Set the framework preset to "Other"
4. Deploy the project

The application is a single HTML file with no external dependencies, so it will work immediately after deployment.

## Example CSV Format

```
100
102
98
101
99
103
```

Each line should contain a single numeric value representing a weight measurement.

## Technical Details

- Pure client-side implementation (no server required)
- Uses HTML5 Canvas for image generation
- Responsive design that works on all device sizes
- Black and white color scheme suitable for printing on supplement boxes
- All processing happens in the browser for privacy and security