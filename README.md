# CamRAW on-device models

Immutable model resources for CamRAW. App source code is not hosted here.

Download individual files from the `models-v1-20261113` Release. The app pins the exact file length and SHA-256 in `manifest.json` and `SHA256SUMS`. The files are byte-identical to the models previously bundled in CamRAW; this release changes delivery only, not inference.

| Files | Purpose |
| --- | --- |
| sam-encoder.onnx + sam-decoder.onnx | SAM selection (both files required) |
| sky.ms | Sky selection |
| depth_anything_v2_vits.onnx | Depth selection, fog and lens blur (shared) |
| moge-2-vits-normal-onnx.onnx | Relighting |
| nind-v1.om | NIND denoising on compatible NNRT devices |

## Provenance and notices

See the attached original NOTICE, SOURCE and LICENSE documents for exact provenance and transformations. SAM: Apache-2.0; Depth Anything V2 Small: Apache-2.0; MoGe-2: upstream MIT and Apache-2.0 notices. Existing provenance records do not separately establish the Sky and NIND trained-checkpoint redistribution licenses; code licenses must not be substituted for weight licenses. No new license grant or clearance is asserted by this repository. The NIND GPL text relates to its upstream code, as explained in NIND_SOURCE.json.

Do not substitute upstream floating/latest models for these files. Model formats, preprocessing, tensor contracts and output algorithms belong to the app and are unchanged. Please verify downloaded bytes against SHA256SUMS.
