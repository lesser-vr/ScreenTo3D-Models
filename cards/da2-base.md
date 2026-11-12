# Depth Anything V2 Base — ScreenTo3D conversion

- Authors: Lihe Yang, Bingyi Kang, Zilong Huang, Zhen Zhao, Xiaogang Xu,
  Jiashi Feng and Hengshuang Zhao (Depth Anything V2).
- Original model: https://huggingface.co/depth-anything/Depth-Anything-V2-Base
- Source: https://github.com/DepthAnything/Depth-Anything-V2
- License: [CC BY-NC 4.0](../licenses/CC-BY-NC-4.0.txt),
  https://creativecommons.org/licenses/by-nc/4.0/.
- Original work and conversion are provided without warranties under that license.
  No affiliation with or endorsement by the original authors is implied.

ScreenTo3D converted the verified Base weights to fixed-shape mixed-FP16 ONNX.
Resize, LayerNormalization and Softmax remain FP32. The two graphs use input
`[1,3,518,896]` and `[1,3,518,924]`, with FP32 input/output. The ZIP includes one
numeric reference per profile for checking locally generated TensorRT engines.
The model/weights are not relicensed by this conversion. Non-commercial conditions
apply to use and redistribution, including modified formats. Commercial-purpose
integration requires appropriate permission from the rights holders.

Source/weight revisions, archive and member hashes are in `../model-manifest.json`.
These provenance records supplement the existing in-archive `NOTICE.txt`.
