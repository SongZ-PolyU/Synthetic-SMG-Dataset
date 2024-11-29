# Synthetic-SMG-Dataset
## from "Synthesizing Real-Time Ultrasound Images of Muscle Based on Biomechanical Simulation and Conditional Diffusion Network"
Multi-task Synthetic SMG Dataset

### Synthesizing pipeline



Our synthesizing pipeline consists of three key stages: 
* (1) **Real-time muscle deformation simulation:** The muscle FEM model was adopted in the first stage to simulate the real deformation of muscle along with true SMG features.
* (2) **Fascicle simulation:** The full fascicle mask captured from the FEM model was converted to a sparse one according to the real distribution to simulate the partially visible appearance of the fascicle in longitudinal sonogram.
* (3) **Ultrasound image generation:** The trained SMG-diffusion would generate high-fidelity ultrasound images based on the structural information in the muscle map.

<div align=center><img src="https://github.com/SongZ-PolyU/Synthetic-SMG-Dataset/blob/main/simple_overview.jpg" width="50%"/></div>

Following our synthesizing pipeline, combinations of settings in different stages were adopted to generate a relatively large SMG dataset with variable real-time muscle morphology, eventually obtaining 3,030 muscle maps, i.e., ground truth.

Detailed implementation can be found in [the paper](https://doi.org/10.1109/TUFFC.2024.3445434).

### Dataset usage
* Multiple types of accurate ground truths, i.e., [aponeuosis masks](https://github.com/SongZ-PolyU/Synthetic-SMG-Dataset/blob/main/aponeurosis_masks.zip), [fascicle masks](https://github.com/SongZ-PolyU/Synthetic-SMG-Dataset/blob/main/fascicle_masks.zip), and [true SMG features](https://github.com/SongZ-PolyU/Synthetic-SMG-Dataset/blob/main/true_values.xlsx), are in the root. 

* Ultrasound images are [here](https://drive.google.com/file/d/1_zjxt-LHBW4sJsGrGBdqmNCwMVDQb-5t/view?usp=sharing).

* File naming format: \{Initial pennation angle α\}\_\{Number of sparse fascicles S\}\_\{Initial subcutis thickness ST\}\_\{Step\}\_\{random seed of reconstruction\}


### Citing
Please cite our paper if you find the dataset useful!
```
@ARTICLE{10648656,
  author={Song, Zhen and Zhou, Yihao and Wang, Jianfa and Zong-Hao Ma, Christina and Zheng, Yongping},
  journal={IEEE Transactions on Ultrasonics, Ferroelectrics, and Frequency Control}, 
  title={Synthesizing Real-Time Ultrasound Images of Muscle Based on Biomechanical Simulation and Conditional Diffusion Network}, 
  year={2024},
  volume={71},
  number={11},
  pages={1501-1513},
  keywords={Ultrasonic imaging;Muscles;Task analysis;Pipelines;Finite element analysis;Training;Real-time systems;Diffusion model;finite element;image generation;muscle;sonomyography (SMG);ultrasound},
  doi={10.1109/TUFFC.2024.3445434}}
```
