# Synthetic-SMG-Dataset
## from "Synthesizing Real-Time Ultrasound Images of Muscle Based on Biomechanical Simulation and Conditional Diffusion Network"
Multi-task Synthetic SMG Dataset

### Synthesizing pipeline

<div align=center><img src="https://github.com/SongZ-PolyU/Synthetic-SMG-Dataset/blob/main/simple_overview.jpg" width="80%"/></div>

Our synthesizing pipeline consists of three key stages: (1) real-time muscle deformation simulation, (2) fascicle simulation, and (3) ultrasound image generation. Specifically, in Stage Ⅰ: the muscle FEM model was adopted in the first stage to simulate the real deformation of muscle along with true SMG features. Stage Ⅱ: the full fascicle mask captured from the FEM model was converted to a sparse one according to the real distribution to simulate the partially visible appearance of the fascicle in longitudinal sonogram. Stage Ⅲ: the trained SMG-diffusion would generate high-fidelity ultrasound images based on the structural information in the muscle map.

Following our synthesizing pipeline, combinations of settings in different stages were adopted to generate a relatively large SMG dataset with variable real-time muscle morphology. In the stage of the deformation simulation, we performed finite element simulation on the muscle model under the conditions of obtaining muscle deformation with different displacements in 100 incremental steps. In addition, two initial subcutis thicknesses were considered, i.e., the distance from the top of the capture window to superficial aponeurosis. In stage Ⅱ, to synthesize the SMG dataset with more variability on fascicle distribution and orientation, five random fascicle reconstructions were performed according to three sparsity levels, eventually obtaining 3,030 muscle maps, i.e., ground truth




File naming format: \{Initial pennation angle α\}\_\{Number of sparse fascicles S\}\_\{Initial subcutis thickness ST\}\_\{Step\}\_\{random seed of reconstruction\}

Our synthetic SMG dataset includes Ultrasound images, aponeruosis masks, fascicle masks, and true SMG features.

Ultrasound images, aponeruosis masks, fascicle masks will be available after publication of relevant paper.
