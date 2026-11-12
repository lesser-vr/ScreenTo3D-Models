# Video Depth Anything Small — ScreenTo3D conversion

- Original model: https://huggingface.co/depth-anything/Video-Depth-Anything-Small
- Source and authors: https://github.com/DepthAnything/Video-Depth-Anything
- License: [Apache 2.0](../licenses/VDA-Apache-2.0.txt),
  https://www.apache.org/licenses/LICENSE-2.0.
- The original license/disclaimer is retained. No affiliation with or endorsement
  by the original authors is implied.

ScreenTo3D adapted the model for streaming warmup/cached ONNX inference with
explicit temporal state, fixed 518x896/924 profiles, stable attention arithmetic,
mixed-FP16 encoder projections and spatial attention. Temporal layers, cache
bindings and depth output remain FP32. There are four graphs and two small
numerical reference files. No original video frames or prebuilt GPU engines are
included. The source/weight revisions and exact file identities are recorded in
`../model-manifest.json`.

Redistribution keeps the original Apache license, relevant copyright/NOTICE
information and these modification notices. The ZIP already includes its source
`LICENSE.txt` and conversion `NOTICE.txt`. The external provenance/card supplements
these immutable original pack files; it does not change the pack's hash.

Only VDA **Small** is covered by this card. No claim about another variant's
license or performance is made. The app validates final-depth samples and applies
its named `vda-fp16-cache-v1` contract to intermediate cache samples. A successful
numerical check does not establish pixel identity or physical stereo quality.
