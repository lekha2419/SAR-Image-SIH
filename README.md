# SAR-Image-SIH
This Repository contains the project we made in the Smart India Hackathon 2024 for the problem statement Converting Synthetic Aperture Radar Image into High Dimensional RGB Colored Image Using Deep Learning.
# SAR-to-Optical Image Translation
Translating grayscale Sentinel-1 SAR satellite images into RGB optical images using deep learning. Two approaches are compared: a conditional GAN and a fully-connected ANN.
# Results
Training progression (SAR input → Ground truth → Generated):
epoch_000.png
epoch_060.png
epoch_196.png
epoch_199.png
# Models
SARGAN — UNet generator + PatchGAN discriminator trained with adversarial + L1 + SSIM loss.
SARANN — Fully-connected ANN baseline. Memory-intensive; hits OOM on a 15 GB GPU at 256×256 resolution.
# Dataset
Paired Sentinel-1 (SAR) and Sentinel-2 (optical) images over Indian terrain — cities, rivers, reservoirs, and mountains. Test locations include Bhopal, Kolkata, and Dehradun.
# Usage
bash: pip install torch torchvision piq pillow matplotlib tqdm
Open SARGAN1.ipynb or SARANN.ipynb in Google Colab with a GPU runtime and run all cells.
# Metrics
Location - Bhopal
SSIM - 0.0152
PSNR - 5.58dB
