# tangible-anatomy-supplementary-material
Supplementary Material for "Adaptive Volumetric Anatomy Visualization in VR with Tangible Control"

This repository builds upon the [work by Matias Lavik](https://github.com/mlavik1/UnityVolumeRendering) and contains: 
- **Direct Volume Rendering (DVR) Shader**: Adapted for Foveated Rendering and Shadows. DVR samples a volume along each pixel's view ray, converting density to RGBA. Phong shading is applied using the volume's gradient, with samples combined using alpha compositing. Foveated Rendering scales the maximum sample count based on the angle between a sampled ray direction and the user's eye-gaze, improving performance without compromising perceived quality.

- **Compute Shader for Volumetric Shadow Precomputation**: Generates a 3D texture of shadow values for DVR. Shadows are determined by integrating the volume's transmittance along a light ray.
