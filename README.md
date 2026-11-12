# ScreenTo3D model packs

Converted model artifacts for [ScreenTo3D](https://github.com/lesser-vr/ScreenTo3D).
These are community conversions, not official releases by the original model authors.
Application source and Windows app releases belong in the application repository.
Large model ZIPs are attached to this repository's Releases, not committed to Git.

| Pack | Download size | Model license |
| --- | ---: | --- |
| [DA2 Base](cards/da2-base.md) | 392,348,171 bytes | **CC BY-NC 4.0: non-commercial use** |
| [VDA Small](cards/vda-small.md) | 363,291,834 bytes | Apache 2.0 |

## Download and installation

Use the versioned release linked by the ScreenTo3D application. No GitHub account
or token is required to download published public assets. The app verifies size
and SHA-256, caches downloads, and builds TensorRT engines for the local GPU.
Selecting a model does not download it until an explicit installation/start action.
Offline users can select the original ZIP using the app's **Install from file**.

These packs contain fixed-shape ONNX graphs and small numerical reference arrays.
They do not contain executable TensorRT engines, NVIDIA libraries, input videos,
or the application. DA2 Small stays in the app; TensorRT/CUDA, FFmpeg and optional
VFG download from their publisher endpoints.

`model-manifest.json` records archive/graph/reference identities and upstream
provenance. `SHA256SUMS.txt` covers release files. The app's own pinned identities
remain its authority; a changed remote manifest cannot authorize different bytes.
Published versioned files must not be replaced with different contents.

## Licensing and compatibility

Each model retains its own license; this is not a repository-wide Apache/MIT grant.
Keep the original attribution, model-specific license, disclaimers and conversion
notices when redistributing. Converting Base to ONNX/FP16 does not remove its
non-commercial restriction. A free download alone does not establish that a
particular commercial integration is permitted.

Both packs use 518x896 and 518x924 inference canvases. The app fits other source
aspect ratios into a canvas. Base uses mixed FP16; VDA uses mixed FP16 encoder
projections/spatial attention and FP32 temporal state. Validation used Windows,
TensorRT 11.2.1.2 and RTX 5090; local compilation is not certification of every GPU.
Preparation includes numerical checks and fails explicitly if validation fails.
These are not universal image-quality or performance guarantees.

## 한국어

ScreenTo3D용 변환 모델 팩 공개 배포 저장소입니다. 앱 소스·실행파일은 앱 저장소,
모델 ZIP은 이 저장소의 Releases에서 제공합니다. 원저작자의 공식 변환본은 아닙니다.
로그인 없이 다운로드할 수 있고, 앱이 크기·해시 확인 후 사용자 GPU용 엔진을 만듭니다.
Base는 **비상업용 조건**, VDA Small은 Apache 2.0을 유지합니다. 자세한 출처·변경
내용은 모델별 카드와 manifest를 확인하세요. NVIDIA 런타임·영상·앱 소스는 동봉하지 않습니다.
