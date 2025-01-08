<div align="center">
  <img src="readme-assets/icon.png" width="200" height="200">
  <h1>Icons</h1>
  <p>Generate beautiful app icons using Flux AI image generation</p>
</div>

<br><br>

Icons is a Python tool that generates app icons using Flux 1.1 Pro on Replicate. It creates icons from text prompts or processes existing images, outputting them as SVG and PNG files.

<br>

## Installation

### Prerequisites

- Python 3.6+
- libvips (required for image processing) - [Installation Guide](https://www.libvips.org/install.html)

### Python Dependencies

Install the required Python packages:

```bash
pip install pyvips replicate colorama python-dotenv tqdm
```

### Configuration

1. Get your Replicate API token from [replicate.com](https://replicate.com)
2. Create a `.env` file in the project root:
   ```
   REPLICATE_API_TOKEN=your_token_here
   ```
   Alternatively, set it as an environment variable.

<br>

## Usage

### Generating a New Icon

1. Run the script:
   ```bash
   python generate.py
   ```
2. Enter your prompt when asked
3. The script will generate:

   - `icons/{timestamp}.svg` - SVG version
   - `icons/{timestamp}.png` - PNG version

   Note: Generated images are temporarily stored in `generations/{timestamp}.jpg`

### Processing an Existing Image

To process an existing image:

```bash
python generate.py --previous path/to/your/image.jpg
```

This will convert your image to SVG and PNG formats in the `icons` directory.

<br>

## Output

The script creates two directories:

- `generations/` - Stores intermediate generated images
- `icons/` - Stores the final icons in SVG and PNG formats

Each file is named with a timestamp for unique identification.
