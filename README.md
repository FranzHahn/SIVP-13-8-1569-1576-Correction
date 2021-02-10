# SIVP-13-8-Correction

This project contains code to reproduce the results published in [Critical analysis on the reproducibility of visual quality assessment using deep features](https://arxiv.org/abs/2009.05369). 

The `main` scripts are the entry point for the reproduction of results. The `_ft` suffix designates fine-tuning, while the `_shuffle` suffix designates a routine that includes shuffling of the inputs for the training of the LSTMs. The code requires a `videos/` folder with the KoNViD-1k videos either in the root directory, or in the sister directory `../nepl/videos/` in case you already downloaded the code from [here](https://github.com/FranzHahn/NPL-50-3-2595-2608-Correction). If not, the videos can be downloaded as a tarball [here](https://datasets.vqa.mmsp-kn.de/plosone/nepl/videos.tar.gz).

By running the code several derivative datastructures are created. These derivatives, except for the `results/` subdirectory, are identical to the ones from the previously mentioned NPL-50-3 Correction repository. The code attempts to re-use them from the sister directory `../nepl/`. If they aren't either in the root directory or this sister directory, they can be downloaded here, as they have been pre-computed by us:

- `frames/`: all the individual video frames are extracted here. [Download](https://datasets.vqa.mmsp-kn.de/plosone/nepl/frames.tar.gz)
- `networks/`: fine-tuned networks are saved here. [Download](https://datasets.vqa.mmsp-kn.de/plosone/nepl/networks.tar.gz)
- `features/`: features for all videos extracted from the networks (with and without fine-tuning) are stored here. [Download](https://datasets.vqa.mmsp-kn.de/plosone/nepl/features.tar.gz)
- `results/`: results of the trained LSTMs are saved here. [Download](https://datasets.vqa.mmsp-kn.de/plosone/sivp/results.tar.gz)

The `results.m` script reproduces the values in rows 10 and 17-20 in Table 2 in the paper, also reproduced below.

![Results Table](https://github.com/FranzHahn/NPL-50-3-2595-2608-Correction/raw/master/figures/resulttable.png "Results Table")