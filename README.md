# LUME TTS model assets

This public repository contains licensed model assets only. Application code and article data are not included.

## Kokoro CoreAI 8-bit vocoder v1

[Download the ZIP](https://github.com/ms-ponyo/lume-tts-models/releases/download/kokoro-coreai-w8-v1/kokoro-coreai-en-zh-w8.zip) · [File/hash manifest](https://github.com/ms-ponyo/lume-tts-models/releases/download/kokoro-coreai-w8-v1/kokoro-coreai-w8.json)

128,253,640-byte download; SHA-256 `3a767b517076a54db5e6c5d8b5cbcbec0ab4aea9c6fbfafaeb84be0be13a7558`. Unpacked model/voices/attribution: 148,592,437 bytes before the small manifest and system compiled cache.

Kokoro v1.0 pretrained weights, exported for native Apple CoreAI CPU execution: FP16 predictor/prosody, weight-only 8-bit vocoder, float32 normalization/DSP and source projection. Includes 20 American English and 8 Mandarin voice packs. Requires a compatible native CoreAI implementation on iOS/macOS 27.

The exported graph has 128 token slots including boundaries and 512 frames (12.8 seconds). A caller must re-split token or duration overflow without dropping the suffix. This is an export choice rather than a fundamental model sentence limit.

Licenses and source revisions are retained inside the ZIP: Kokoro checkpoint/model voices Apache-2.0, graph-authoring recipe BSD-3-Clause. Source checkpoint: hexgrad/Kokoro-82M revision f3ff3571791e39611d31c381e3a41a3af07b4987. Authoring recipe adapted from john-rocky/coreai-model-zoo revision aa6c940958b439b6649ce53d3f101288a4525675. The full manifest names and hashes each file.

## Pocket CoreAI compact English v1

[Download the all-voice package](https://github.com/ms-ponyo/lume-tts-models/releases/download/pocket-coreai-compact-v1/pocket-coreai-english-v1.zip) · [Manifest](https://github.com/ms-ponyo/lume-tts-models/releases/download/pocket-coreai-compact-v1/pocket-coreai-compact.json)

184,519,201-byte ZIP; SHA-256 `fc20595e4c4d20cc17b44609206a8bed7242b75bf80cc177fc92fd235802fe4e`. Unpacked model, all eight English voices and attribution: 246,592,049 bytes before compiler caches. The original neural graphs are unchanged; this removes the redundant full checkpoint and stores voice KV seeds at their existing FP16 runtime precision. Native Mac tests generated identical PCM for every preset.

Derived from Kyutai Pocket TTS revision e041936c75475d350b405bc870bcf7c22da4e9e6 (CC-BY-4.0), converted CoreAI graphs d774360b912aa70d217e34204cef1cebfdadadd1 and the RahulRachuri/pocket-tts-swift port (Apache-2.0). Full attribution is inside the package. No new training, custom voice cloning, app source or article data is included.
