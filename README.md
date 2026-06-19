# Product Advertisement Generation

## Project Description
This project leverages generative AI to create compelling product advertisements. It combines Stable Diffusion for generating product images and a large language model (Phi-3-mini) for generating video explainer scripts.

## Features
- **AI-powered Image Generation**: Generate high-quality product images from text prompts using Stable Diffusion.
- **Script Generation**: Create engaging 60-second product explainer video scripts with a large language model.
- **Customization**: Easily modify product names, prompts, and script content to fit different advertising needs.
- **Output**: Save generated images and video scripts for further use.

## How to Use
1.  **Install Dependencies**: Run the first few cells to install necessary libraries (`diffusers`, `transformers`, `accelerate`, `moviepy`, etc.).
2.  **Initialize Models**: The notebook sets up a `StableDiffusionPipeline` for image generation and a `pipeline` for text generation (using `microsoft/Phi-3-mini-4k-instruct`).
3.  **Generate Product Images**: 
    - Modify the `product_name` and `prompt` variables to describe your desired product and advertisement style.
    - Execute the image generation cells to create and display product images.
    - The images will be saved as `product_image.png` and other numbered `.png` files for different prompts.
4.  **Generate Explainer Video Script**: 
    - Update the `product_description` with details about your product.
    - Run the script generation cells to obtain a 60-second video explainer script.
5.  **Generate Final Video (Requires avatar_video.mp4)**: 
    - Ensure you have an `avatar_video.mp4` file in the same directory (or specify its path).
    - The final cell will combine the script (not directly, but implies a video generation step based on a placeholder video) and save it as `final_product_explainer.mp4`.

## Dependencies
- `diffusers`
- `transformers`
- `accelerate`
- `safetensors`
- `torch`
- `moviepy`
- `Pillow` (PIL)

## Note
- The script generation uses `microsoft/Phi-3-mini-4k-instruct` which is a relatively small but capable model.
- For video generation, an `avatar_video.mp4` is expected as a placeholder. In a real-world scenario, you would integrate a text-to-speech and video synthesis service.
