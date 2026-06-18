# Robust Image DNA Storage Pipeline v7

This version adds compression level and advanced settings for all four compression methods.

## Panel 2 compression methods

1. No compression
   - No compression level.
   - Uses selected raw pixel data directly.
   - Black-white remains packed as 1 bit/pixel.

2. Robust Low-Resolution
   - Compression level:
     - High quality
     - Balanced
     - High compression
     - Custom
   - Advanced settings:
     - Downsample
     - Bits per channel

3. Base + Local Detail
   - Compression level:
     - High quality
     - Balanced
     - High compression
     - Custom
   - Advanced settings:
     - Base downsample
     - Base bits
     - Keep coefficients
     - Coefficient bits
     - Residual q step

4. Base + WebP Detail
   - Compression level:
     - High quality
     - Balanced
     - High compression
     - Custom
   - Advanced settings:
     - WebP quality
     - Tile size
     - Base downsample
     - Base bits

5. Local Block Coding
   - Compression level:
     - High quality
     - Balanced
     - High compression
     - Custom
   - Advanced settings:
     - Y q scale
     - C q scale
     - Y packet bits
     - C packet bits

## Preserved from v6

- Reconstruction source selector:
  - Original encoded data
  - Noisy encoded data
  - Sequencing rebuilt data

- Advanced sequencing simulation is optional and collapsed.

- Panel 2 still reports:
  - Image size
  - Raw pixel data
  - Payload/compressed size
  - Compression ratio
  - PSNR / SSIM where available

## Smoke tests

All methods and presets were tested through:

payload generation -> Simple Mapping DNA Design -> DNA decoding -> image reconstruction.
