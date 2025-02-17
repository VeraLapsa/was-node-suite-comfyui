# WAS's Comprehensive Node Suite [![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FWASasquatch%2Fwas-node-suite-comfyui&count_bg=%233D9CC8&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)

![image](https://user-images.githubusercontent.com/1151589/227418056-d6928b42-2492-414c-9c16-21e50d976cf5.png) 

### A node suite for [ComfyUI](https://github.com/comfyanonymous/ComfyUI) with many new nodes, such as image processing, text processing, and more. 

### I am looking for people who would like to share what they have come created using these nodes. Feel free to PR to the `/workflows/` directory. Only `.json` and image files, please. 

1. Current Nodes:
    - CLIPTextEncode (NSP): Parse Noodle Soup Prompts
    - Constant Number
    - Debug to Console (Debug pretty much anything to the console window)
    - Image Blank: Create a blank image in any colo
    - Image Blend by Mask: Blend two images by a mask
    - Image Blend: Blend two images by opacity
    - Image Blending Mode: Blend two images by various blending modes
    - Image Bloom Filter: Apply a high-pass based bloom filter
    - Image Canny Filter: Apply a canny filter to a image
    - Image Chromatic Aberration: Apply chromatic aberration lens effect to a image like in sci-fi films, movie theaters, and video games
    - Image Edge Detection Filter: Detect edges in a image
    - Image Film Grain: Apply film grain to a image
    - Image Filter Adjustments: Apply various image adjustments to a image
    - Image Flip: Flip a image horizontal, or vertical
    - Image High Pass Filter: Apply a high frequency pass to the image returning the details
    - Image Levels Adjustment: Adjust the levels of a image
    - Image Load: Load a *image* from any path on the system, or a url starting with `http`
    - Image Median Filter: Apply a median filter to a image, such as to smooth out details in surfaces
    - Image Mix RGB Channels: Mix together RGB channels into a single iamge
    - Image Nova Filter: A image that uses a sinus frequency to break apart a image into RGB frequencies
    - Image Remove Background (Alpha): Remove the background from a image by threshold and tolerance. 
    - Image Remove Color: Remove a color from a image and replace it with another
    - Image Resize
    - Image Rotate: Rotate an image
    - Image Save: A save image node with format support and path support. (Bug: Doesn't display image
    - Image Select Channel: Select a single channel of an RGB image
    - Image Select Color: Return the select image only on a black canvas
    - Image Style Filter: Style a image with Pilgram instragram-like filters
    - Image Threshold: Return the desired threshold range of a image
    - Image Transpose
    - Image fDOF Filter: Apply a fake depth of field effect to an image
    - Image to Latent Mask: Convert a image into a latent mask
    - Input Switch  (Disable until `*` wildcard fix)
    - KSampler (WAS): A sampler that accepts a seed as a node inpu
    - Load Text File
    - Load Batch Images
      - Increment images in a folder, or fetch a single image out of a batch.
      - Will reset it's place if the path, or pattern is changed.
      - pattern is a glob that allows you to do things like `**/*` to get all files in the directory and subdirectory
        or things like `*.jpg` to select only JPEG images in the directory specified. 
    - Latent Noise Injection: Inject latent noise into a latent image
    - Latent Upscale by Factor: Upscale a latent image by a facto
    - MiDaS Depth Approximation: Produce a depth approximation of a single image input
    - MiDaS Mask Image: Mask a input image using MiDaS with a desired color
    - Number Operation
    - Number to Seed
    - Random Number
    - Save Text File: Save a text string to a file
    - Seed: Return a seed
    - Tensor Batch to Image: Select a single image out of a latent batch for post processing with filters
    - Text Concatenate: Merge two strings
    - Text Find and Replace: Find and replace a substring in a string
    - Text Multiline: Write a multiline text strin
    - Text Parse Noodle Soup Prompts: Parse NSP in a text input
    - Text Random Line: Select a random line from a text input string
    - Text String: Write a single line text string value
    - Text to Conditioning: Convert a text string to conditioning.

## Recommended Installation:
If you're running on Linux, or non-admin account on windows you'll want to ensure `/ComfyUI/custom_nodes`, `was-node-suite-comfyui`, and `WAS_Node_Suite.py` has write permissions.

  - Navigate to your `/ComfyUI/custom_nodes/` folder
  - `git clone https://github.com/WASasquatch/was-node-suite-comfyui/`
  - Start ComfyUI
    - WAS Suite should uninstall legacy nodes automatically for you.
    - Tools will be located in the WAS Suite menu.
    
## Alternate Installation:
If you're running on Linux, or non-admin account on windows you'll want to ensure `/ComfyUI/custom_nodes`, and `WAS_Node_Suite.py` has write permissions.

  - Download `WAS_Node_Suite.py`
  - Move the file to your `/ComfyUI/custom_nodes/` folder
  - Start, or Restart ComfyUI
    - WAS Suite should uninstall legacy nodes automatically for you.
    - Tools will be located in the WAS Suite menu.
      
### Dependencies:
WAS Node Suite is designed to download dependencies on it's own as needed, but what it depends on can be installed manually before use to prevent any script issues. The dependencies which are not required by ComfyUI are as follows: 
  - opencv
  - scipy
  - pilgram
  - timm (for MiDaS)
    - MiDaS Models (they will download automatically upon use and be stored in `/ComfyUI/models/midas/checkpoints/`, additional files may be installed by `PyTorch Hub`)

*This version renames some nodes, as well as introduces new fields. Unfortunately ComfyUI doesn't handle these changes well, so you'll have to replace the dreaded "red nodes" manually.*
