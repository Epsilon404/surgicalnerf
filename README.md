# A Review of 3D Reconstruction of Deformable Tissues in Robotic Surgery

Paper for [MICCAI 2024 Workshop: Embodied AI and Robotics for HealTHcare (EARTH)](https://earth-workshop.github.io/)

## Related Works
Please follow the readme files of the following 4 models for environment installation and data processing to reproduce their results.
- EndoNeRF: [EndoNeRF README](https://github.com/Epsilon404/surgicalnerf/tree/main/EndoNeRF#neural-rendering-for-stereo-3d-reconstruction-of-deformable-tissues-in-robotic-surgery)
- EndoSurf: [EndoSurf README](https://github.com/Epsilon404/surgicalnerf/tree/main/endosurf#endosurf-neural-surface-reconstruction-of-deformable-tissues-with-stereo-endoscope-videos)
- LerPlane: [LerPlane README](https://github.com/Epsilon404/surgicalnerf/tree/main/ForPlane#offical-code-implementation-for-forplane-and-lerplane)
- 4D-GS: [4DGaussians README](https://github.com/Epsilon404/surgicalnerf/tree/main/4DGaussians#4d-gaussian-splatting-for-real-time-dynamic-scene-rendering)

## Dataset Preperation
1. EndoNeRF dataset: Please fill in this form [[Sample Dataset for EndoNeRF]](https://forms.gle/1VAqDJTEgZduD6157) to download EndoNeRF dataset.
2. StereoMIS dataset: Please download the StereoMIS dataset from [here](https://zenodo.org/records/8154924), then process the data by [Robust Camera Pose Estimation for Endoscopic Videos](https://github.com/aimi-lab/robust-pose-estimator?tab=readme-ov-file#prepare-the-data), and organize it in the structure as EndoNeRF:
    ```
    + data1
        |
        |+ depth/           # depth maps
        |+ masks/           # binary tool masks
        |+ images/          # rgb images
        |+ pose_bounds.npy  # camera poses & intrinsics in LLFF format
    ```
    Stereo depth maps are obtained by [STTR-Light](https://github.com/mli0603/stereo-transformer/tree/sttr-light). You can also generate monocular depth maps by [Dpeth-Anything](https://huggingface.co/LiheYoung/depth-anything-large-hf).
3. C3VD dataset: Please download the C3VD dataset from [here](https://durrlab.github.io/C3VD/) and the depth map is included in the dataset.

## Acknowledgements
We would like to acknowledge the following excellent works: [EndoNeRF](https://github.com/med-air/EndoNeRF)(Wang et al.), [EndoSurf](https://github.com/Ruyi-Zha/endosurf)(Zha et al.), [LerPlane](https://github.com/Loping151/ForPlane)(Yang et al.), [4D-GS](https://github.com/hustvl/4DGaussians)(Wu et al.).
