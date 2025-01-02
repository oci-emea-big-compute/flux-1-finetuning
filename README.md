# flux-1-finetuning

This repo is designed to quickly  prepare a demo that showcases how to use OCI GPU shapes to finetune lora models of flux.1-dev. 

Flux is a set of diffusion models created by BlackForest Labs, and are subject to [licensing terms](https://github.com/black-forest-labs/flux/blob/main/model_licenses/LICENSE-FLUX1-dev)
In this blog we will show how to fine tune flux.1-dev that is available in [HuggingFace](https://huggingface.co/black-forest-labs/FLUX.1-dev)

There are several projects that can be used to work with flux models
- [ComfyUI](https://github.com/comfyanonymous/ComfyUI) is a powerful and user-friendly tool for creating high-quality images using AI, including the FLUX model. It offers a modular workflow design that allows users to create custom image generation processes by connecting different components
- [AItoolkit](https://github.com/comfyanonymous/ComfyUI) is a tool that simplifies Flux fine tuning experience expoecially to reduce VRAM requirements. 
- [SimpleTuner](https://github.com/bghira/SimpleTuner) is a set of scripts that simplify distributed fine tuning on multiple GPUs 

Prerequisites: 
- Linux based GPU VM with recent Nvidia driver and Cuda toolkit
- git, Miniconda installed

## Installing AI toolkit ##

use aitoolkit.yaml  to prepare a conda environment with the required packages 

```
conda create env -f aitoolkit.yaml
conda activate aitoolkit
```

then you can clone the ai-toolkit 
```
git clone https://github.com/ostris/ai-toolkit.git
cd ai-toolkit
git submodule update --init --recursive
```

## Dataset generation ##

WIP
you can take 10 pictures of yourself .


## Training

Aitoolkit has a large set of options that can be exploited to train a lora model for flux1. You can fin examples in the directory config/examples/.
According to the different GPUs you can use them to eitther reduce video memory consumption, or to improve training performance. 







