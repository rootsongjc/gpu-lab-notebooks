# GPU Lab Notebooks

Google Colab notebooks for the **Colab Primer** of the book *GPU Lab on Kubernetes* ([中文](https://jimmysong.io/zh/book/gpu-lab-on-kubernetes/); English edition coming).

The primer builds single-machine GPU intuition before the Kubernetes/HAMi chapters: nvidia-smi, PCIe, the CUDA driver/runtime/toolkit split, VRAM and the caching allocator, GPU utilization semantics, NVML, the CUDA programming model, a first CUDA C++ kernel, multi-process sharing with MPS, the MIG/MPS/time-slicing/vGPU landscape, and finally why Kubernetes needs a device plugin.

## Requirements

- A Google account and a browser. No local GPU, no cloud account, no driver installation.
- Every lab targets the free **Tesla T4** runtime: *Runtime → Change runtime type → T4 GPU*.
- Each lab is a 10–30 minute, self-contained notebook so it survives Colab's session limits.

## Labs

| # | Chapter | Notebook | Open |
| :-- | :--- | :--- | :--- |
| 01 | [Meet Your GPU: nvidia-smi and the Tesla T4](https://jimmysong.io/zh/book/gpu-lab-on-kubernetes/colab/lab-01-meet-your-gpu/) | [`lab-01-meet-your-gpu.ipynb`](labs/lab-01-meet-your-gpu.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rootsongjc/gpu-lab-notebooks/blob/main/labs/lab-01-meet-your-gpu.ipynb) |
| 02 | [What a GPU Looks Like: lspci and PCIe Topology](https://jimmysong.io/zh/book/gpu-lab-on-kubernetes/colab/lab-02-gpu-on-pcie/) | [`lab-02-gpu-on-pcie.ipynb`](labs/lab-02-gpu-on-pcie.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rootsongjc/gpu-lab-notebooks/blob/main/labs/lab-02-gpu-on-pcie.ipynb) |
| 03 | [Does CUDA Exist? Driver, Runtime and Toolkit](https://jimmysong.io/zh/book/gpu-lab-on-kubernetes/colab/lab-03-cuda-exists/) | [`lab-03-cuda-exists.ipynb`](labs/lab-03-cuda-exists.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rootsongjc/gpu-lab-notebooks/blob/main/labs/lab-03-cuda-exists.ipynb) |
| 04 | [Where Did the VRAM Go? Tensors and nvidia-smi](https://jimmysong.io/zh/book/gpu-lab-on-kubernetes/colab/lab-04-where-did-vram-go/) | [`lab-04-where-did-vram-go.ipynb`](labs/lab-04-where-did-vram-go.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rootsongjc/gpu-lab-notebooks/blob/main/labs/lab-04-where-did-vram-go.ipynb) |
| 05 | [GPU Utilization: Why Is It Always 0%?](https://jimmysong.io/zh/book/gpu-lab-on-kubernetes/colab/lab-05-gpu-utilization/) | [`lab-05-gpu-utilization.ipynb`](labs/lab-05-gpu-utilization.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rootsongjc/gpu-lab-notebooks/blob/main/labs/lab-05-gpu-utilization.ipynb) |
| 06 | [NVML: Reading GPU State from Python](https://jimmysong.io/zh/book/gpu-lab-on-kubernetes/colab/lab-06-nvml/) | [`lab-06-nvml.ipynb`](labs/lab-06-nvml.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rootsongjc/gpu-lab-notebooks/blob/main/labs/lab-06-nvml.ipynb) |
| 07 | [The CUDA Programming Model: From CPU Thinking to GPU Thinking](https://jimmysong.io/zh/book/gpu-lab-on-kubernetes/colab/lab-07-cuda-programming-model/) | [`lab-07-cuda-programming-model.ipynb`](labs/lab-07-cuda-programming-model.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rootsongjc/gpu-lab-notebooks/blob/main/labs/lab-07-cuda-programming-model.ipynb) |
| 08 | [Your First CUDA Kernel](https://jimmysong.io/zh/book/gpu-lab-on-kubernetes/colab/lab-08-cuda-kernel/) | [`lab-08-cuda-kernel.ipynb`](labs/lab-08-cuda-kernel.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rootsongjc/gpu-lab-notebooks/blob/main/labs/lab-08-cuda-kernel.ipynb) |
| 09 | [MPS: Why a GPU Can Be Shared](https://jimmysong.io/zh/book/gpu-lab-on-kubernetes/colab/lab-09-mps/) | [`lab-09-mps.ipynb`](labs/lab-09-mps.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rootsongjc/gpu-lab-notebooks/blob/main/labs/lab-09-mps.ipynb) |
| 10 | [GPU Virtualization Landscape: MIG, MPS, Time-slicing and vGPU](https://jimmysong.io/zh/book/gpu-lab-on-kubernetes/colab/lab-10-gpu-virtualization/) | [`lab-10-gpu-virtualization.ipynb`](labs/lab-10-gpu-virtualization.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rootsongjc/gpu-lab-notebooks/blob/main/labs/lab-10-gpu-virtualization.ipynb) |
| 11 | [Bridging to Kubernetes: Why a Device Plugin Is Needed](https://jimmysong.io/zh/book/gpu-lab-on-kubernetes/colab/lab-11-bridge-to-k8s/) | [`lab-11-bridge-to-k8s.ipynb`](labs/lab-11-bridge-to-k8s.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rootsongjc/gpu-lab-notebooks/blob/main/labs/lab-11-bridge-to-k8s.ipynb) |

## How these notebooks are built

The notebooks are **generated** from the book's chapter sources: every `## ` section becomes a Markdown cell and every ```` ```python ```` fence becomes a code cell, so the code you run here is exactly the code printed in the book. Please report problems against the chapter content (issues here are fine); the `.ipynb` files are regenerated rather than edited by hand.

## Contributing

Each chapter carries a *Metadata Card* with a verification status. If you run a lab on Colab, please open an issue or PR with the date, driver / CUDA versions, key output values and any failure mode you hit, so the expected outputs in the book can be backfilled with real numbers.

## License

Code cells are MIT licensed. Prose is © Jimmy Song, licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).
