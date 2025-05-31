# 🧠 Topological Methods in Diffusion Models：Ideas & Collection

【Topology Information】、【Diffusion models】、【combinatorial problems】【TSP】…… 

This project try to integrate RTD-Lite into diffusion models - as loss, initialization, or input - enables topological-aware optimization for combinatorial problems like TSP and graph generation.

This repository collects and summarizes research works that combine Topological Data Analysis (TDA) with diffusion models, aiming to improve solutions to combinatorial optimization problems such as the Traveling Salesman Problem (TSP).

## Ideas💡
### RTD-Lite as a Loss Function/Regularity
- Goal:Use RTD-Lite as a topological regularizer or loss function in a diffusion-based model
- Form: $\text{Loss} = \hat{\mathcal{O}} + \hat{\mathcal{O}}_{\text{RTD-Lite}}$
- Usage: Encourage the generated solutions to preserve topological structure measured by RTD-Lite.

### RTD-Lite as a Start/Initialization
- Goal: Use RTD-Lite-based structure(e.g., topological-informed graphs) as a warm start for the diffusion model.
- Method: Inject Gaussian noise to perturb RTD-Lite output and initial the diffusion process.

### RTD-Lite as Input Feature/Conditioning
- Goal: Use RTD-Lite features(e.g., Betti numbers or structural summaries) as input to the neural network.
- Setup:
  - Incorporate RTD-Lite into a 10-NN graph with topological annotation.
  - Guide the model to learn difficult configuration by showing RTD-Lite-derived-topologies.
- Model: Conditioned diffusion or IQNN (implicit Quantile Neural Net) with topological input.

## Categories 🧰
### Topology + Diffusion
-  **TopodiffusionNet（TDN）| Topology-based objective function**
Gupta, S., Samaras, D., & Chen, C. (2024). TopoDiffusionNet: A Topology-aware Diffusion Model. arXiv:2410.16646. Retrieved October 01, 2024, from [Paper](https://ui.adsabs.harvard.edu/abs/2024arXiv241016646G) | [Code](https://github.com/Saumya-Gupta-26/TopoDiffusionNet)

-  **Loss function | Betti number** 
Hu, X., Fuxin, L., Samaras, D., & Chen, C. (2019). Topology-Preserving Deep Image Segmentation. arXiv:1906.05404. Retrieved June 01, 2019, from [Paper](https://ui.adsabs.harvard.edu/abs/2019arXiv190605404H)｜ [Code]()

-  **Latent Diffusion Models（LDM）｜Persistent Homology** 
Hu, J., Fei, B., Xu, B., Hou, F., Yang, W., Wang, S., Lei, N., Qian, C., & He, Y. (2024). Topology-Aware Latent Diffusion for 3D Shape Generation. arXiv:2401.17603. Retrieved January 01, 2024, from [Paper](https://ui.adsabs.harvard.edu/abs/2024arXiv240117603H) | [Code]()

- **TopoDiff｜Structural Topology Optimization｜GAN**\
🌟 Mazé, F., & Ahmed, F. (2023). Diffusion Models Beat GANs on Topology Optimization. Proceedings of the AAAI Conference on Artificial Intelligence, 37(8), 9108-9116. [Paper](https://doi.org/10.1609/aaai.v37i8.26093) | [Code](https://decode.mit.edu/projects/topodiff/)

- **Linear Threshold Model（LTM）｜ Supermodularity**
Khalil, E. B., Dilkina, B., & Song, L. (2014). Scalable diffusion-aware optimization of network topology Proceedings of the 20th ACM SIGKDD international conference on Knowledge discovery and data mining, New York, New York, USA. [Paper](https://doi.org/10.1145/2623330.2623704) | [Code]()

- **DiffAN｜Causal discovery｜**
Sanchez, P., Liu, X., O'Neil, A. Q., & Tsaftaris, S. A. (2022). Diffusion Models for Causal Discovery via Topological Ordering. arXiv:2210.06201. Retrieved October 01, 2022, from [Paper](https://ui.adsabs.harvard.edu/abs/2022arXiv221006201S) | [Code](https://github.com/vios-s/DiffAN)

- **TOLDM | Latent Diffusion | Multi-Stage Strategy | Cross-Attention**
Sanchez, P., Liu, X., O'Neil, A. Q., & Tsaftaris, S. A. (2022). Diffusion Models for Causal Discovery via Topological Ordering. arXiv:2210.06201. Retrieved October 01, 2022, from [Paper](https://ui.adsabs.harvard.edu/abs/2022arXiv221006201S) | [Code]()

### Diffusion + TSP 
- **Difusco| TSP**
Sun, Z., & Yang, Y. (2023). Difusco: Graph-based diffusion solvers for combinatorial optimization. Advances in neural information processing systems, 36, 3706-3731.[Paper](https://doi.org/10.48550/arXiv.2302.08224) | [Code](https://github.com/Edward-Sun/DIFUSCO)
- **IDEQ ｜ Hamiltonian tour｜2-opt**
Basson, M., & Preux, P. (2024). IDEQ: an improved diffusion model for the TSP. arXiv:2412.13858. Retrieved December 01, 2024, from [Paper](https://ui.adsabs.harvard.edu/abs/2024arXiv241213858B) | [Code]()

