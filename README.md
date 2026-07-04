Image Generation with Pre-trained Models

This project is Task 2 of my Generative AI Internship at Prodigy InfoTech. The goal was to utilize pre-trained generative models to create images from text prompts, exploring and comparing two different approaches.

📌 Task Overview

Utilize pre-trained generative models like DALL-E Mini or Stable Diffusion to create images from text prompts.

🛠️ Tech Stack


Python 3
Google Colab (T4 GPU)
Hugging Face diffusers — for loading and running image generation pipelines
PyTorch — underlying deep learning framework
Matplotlib — for displaying generated images


🖼️ Methods Used

Method 1: Stable Diffusion v1.5 (Hugging Face Diffusers)

Loaded the runwayml/stable-diffusion-v1-5 model using Hugging Face's diffusers library and generated high-quality images from various text prompts.

How Stable Diffusion works:


Takes a text prompt and converts it into numerical embeddings
Starts from random noise and runs it through a denoising process over 50 steps
Each step gradually refines the noise into a coherent image that matches the prompt
Produces detailed, high-quality 512×512 images


Prompts used:


"a magical forest with glowing mushrooms at night, fantasy art, highly detailed, vibrant colors"
"a beautiful sunset over the ocean, oil painting style"
"a futuristic city at night, neon lights, cyberpunk style"
"cute magical flying dog, fantasy art, golden color, highly detailed"



Method 2: DALL-E Mini Style Generation

Loaded the OFA-Sys/small-stable-diffusion-v0 model as a DALL-E Mini equivalent to generate images using the same prompts for a direct comparison.

How DALL-E Mini works:


Uses a VQGAN + CLIP approach to generate images from text
Lighter and faster than Stable Diffusion
Produces simpler but quicker results


Same prompts used as Method 1 for direct comparison of outputs.


📊 Comparison: Method 1 vs Method 2

FeatureMethod 1 (Stable Diffusion v1.5)Method 2 (DALL-E Mini Style)Model SizeLarge (~4GB)SmallerImage QualityHigh, photorealisticSimpler, fasterGeneration Speed~7 seconds/imageFasterDetail LevelHighly detailedBasicBest forCreative, artistic imagesQuick generation

Conclusion

Stable Diffusion v1.5 produced higher quality, more detailed and visually impressive images. The DALL-E Mini style model was lighter and faster but produced simpler outputs. For high-quality creative image generation from text prompts, Stable Diffusion is the stronger choice.

📁 Repository Contents


Text_to_Picture_Generation.ipynb — complete Colab notebook with both methods, all generated images, and comparison


🚀 How to Run


Open Text_to_Picture_Generation.ipynb in Google Colab
Enable GPU: Runtime → Change runtime type → T4 GPU
Run all cells in order
Modify the prompt variable to generate images from your own text


📚 References


Stable Diffusion in KerasCV — TensorFlow Tutorial
DALL-E Mini Image Generator — Colab Notebook
E-DALL-E: Creating Digital Art — Towards Data Science





✍️ Author

Kaviya Sivakumar


Part of the Generative AI Internship Program — Prodigy InfoTech

----> 2 import keras_cv
      3 from tensorflow import keras
      pasted
