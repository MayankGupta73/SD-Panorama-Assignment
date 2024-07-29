# SD Panorama Assignment

The assignment code uses a Stable Diffusion model for the generation of coherent 360 degree panoramas. 

The assignment implements two parts:

1. Text to img SD model for SD Panorama + Seam Tiling: A stable diffusion model is used for generating panoramas from a given input text prompt. Seam tiling was tried using two ways. Firstly, a panorama stitching approach using keypoint matching was tried but did not work well due to inability to match the keypoints in the edges. The second approach used another SD model for inpainting to remove the inconsistency in the edges.
2. Depth map for conditioning of Panorama: A ControlNet model is used for conditioning generation in the prior step via a depth map. The generated image is also similarly seam tiled to ensure continuity.

## Code
The code used can be accessed and run through the provided Jupyter notebook. All provided code has been run on Google Colab.

## Sample outputs
The sample outputs can be accessed via the `sample_outputs` folder. The part 1 and part 2 regular and seam tiled panoramas for 5 different prompts have been attached. The prompts themselves are present in a txt file in the folder.