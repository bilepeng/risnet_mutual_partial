# RISnet: A Domain-Knowledge Driven Neural Network Architecture for RIS Optimization with Mutual Coupling and Partial CSI

![GitHub](https://img.shields.io/github/license/bilepeng/risnet_mutual_partial)
[![DOI](https://img.shields.io/badge/doi-10.1109/TWC.2025.3536178-informational)](https://doi.org/10.1109/TWC.2025.3536178)
[![arXiv](https://img.shields.io/badge/arXiv-2403.04028-informational)](https://arxiv.org/abs/2403.04028)

This repository is accompanying the paper "RISnet: A Domain-Knowledge Driven
Neural Network Architecture for RIS Optimization with Mutual Coupling and
Partial CSI" (Bile Peng, Karl-Ludwig Besser, Shanpu Shen, Finn
Siegismund-Poschmann, Ramprasad Raghunath, Daniel Mittleman, Vahid Jamali, and
Eduard A. Jorswieck, IEEE Transactions on Wireless Communications, vol. 24, no.
5, pp. 4469-4482, May 2025, [doi:
10.1109/TWC.2025.3536178](https://doi.org/10.1109/TWC.2025.3536178),
[arXiv:2403.04028](https://arxiv.org/abs/2403.04028)).


## File List

The following files are provided in this repository:

- `train.py`: Main file to train the model.
- `core.py`: Core classes of RISnet and data loader.
- `util.py`: Utility functions.



## Usage

Make sure that you have [Python3](https://www.python.org/downloads/) and all
necessary libraries installed on your machine.

Create a folder `data` and download files from https://drive.google.com/file/d/1cXh4ME7bmY7a7llOj4Np2qBakrI2eHwH/view
and put them in the folder.

Create a folder `results`, where the training and testing results will be saved.

Run `python train.py` with the following arguments to train the model:

```bash
python3 train.py --record True  --tsnr=1e12  --partialcsi True --trainingchannelpath data/channels_ris_rx_training.pt --testingchannelpath data/channels_ris_rx_testing.pt --name partial_0
python3 train.py --record True  --tsnr=1e12  --partialcsi False --trainingchannelpath data/channels_ris_rx_training.pt --testingchannelpath data/channels_ris_rx_testing.pt --name full_0
python3 train.py --record True  --tsnr=1e12  --partialcsi True --trainingchannelpath data/channels_ris_rx_training_5e-5.pt --testingchannelpath data/channels_ris_rx_testing_5e-5.pt --name partial_p
python3 train.py --record True  --tsnr=1e12  --partialcsi False --trainingchannelpath data/channels_ris_rx_training_5e-5.pt --testingchannelpath data/channels_ris_rx_testing_5e-5.pt --name full_p
python3 train.py --record True  --tsnr=1e12  --partialcsi True --trainingchannelpath data/channels_ris_rx_training_iid.pt --testingchannelpath data/channels_ris_rx_testing_iid.pt --name partial_iid
python3 train.py --record True  --tsnr=1e12  --partialcsi False --trainingchannelpath data/channels_ris_rx_training_iid.pt --testingchannelpath data/channels_ris_rx_testing_iid.pt --name full_iid
```

You need Tensorboard to illustrate the results.


## Acknowledgements

This research was supported by the Federal Ministry of Education and Research
Germany (BMBF) as part of the 6G Research and Innovation Cluster (6G-RIC) under
Grant 16KISK031.


## License and Referencing
This program is licensed under the GPLv3 license. If you in any way use this
code for research that results in publications, please cite our original
article listed above.

You can use the following BibTeX entry
```bibtex
@article{Peng2025risnet,
  author = {Peng, Bile and Besser, Karl-Ludwig and Shen, Shanpu and Siegismund-Poschmann, Finn and Raghunath, Ramprasad and Mittleman, Daniel and Jamali, Vahid and Jorswieck, Eduard A.},
  title = {RISnet: A Domain-Knowledge Driven Neural Network Architecture for RIS Optimization with Mutual Coupling and Partial CSI},
  journal = {IEEE Transactions on Wireless Communications},
  year = {2025},
  month = {5},
  volume = {24},
  number = {5},
  pages = {4469--4482},
  publisher = {IEEE},
  archiveprefix = {arXiv},
  eprint = {2403.04028},
  primaryclass = {cs.IT},
  doi = {10.1109/TWC.2025.3536178},
}
```
