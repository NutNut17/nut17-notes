---
title: "CUDA"
description: ""
summary: ""
date: 2025-07-09T23:45:01+08:00
lastmod: 2025-07-09T23:45:01+08:00
weight: 504
draft: false
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---

+------------------------------------------------+
|   PyTorch / TensorFlow framework               |
|     (uses CUDA libraries)                      |
+--------------------+---------------------------+
| CUDA Libraries     | cuDNN, cuBLAS, NCCL, etc |
+--------------------+---------------------------+
| CUDA Runtime       | (libcudart, device code) |
+------------------------------------------------+
| HOST NVIDIA Driver | (must be >= runtime ver) |
+------------------------------------------------+
| Physical GPU       |
+------------------------------------------------+

A pytorch with cuda is bundled with CUDA runtime, libraries, PTX kernels, architecture -specifc kernels. Except for NVIDIA driver.

