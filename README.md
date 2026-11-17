# Tilawa models

Files the Tilawa iOS app downloads on first use, so they don't make the app
itself larger. Each one is attached to a release, not stored in the
repository.

## Recitation model

`ggml-base-ar-quran.bin`, in the [model-v1 release](../../releases/tag/model-v1).

- **What it is:** [tarteel-ai/whisper-base-ar-quran](https://huggingface.co/tarteel-ai/whisper-base-ar-quran),
  OpenAI's Whisper base model fine-tuned on Quran recitation, converted for
  [whisper.cpp](https://github.com/ggml-org/whisper.cpp). Tilawa runs it on the
  device, so recitation audio never leaves the phone.
- **Format:** ggml, with 16-bit floating-point weights.
- **Size:** 147,951,465 bytes.
- **SHA-256:** `0a30efbd25c2464360809accb85d8492d48bce2945939405fb800b8281ff2f3c`

The app checks the size and SHA-256 before using a download, so a damaged or
replaced file is rejected.

## Licence

The model is licensed under the Apache License 2.0 (see `LICENSE`), by its
authors at Tarteel AI. Whisper, which it is fine-tuned from, is MIT-licensed by
OpenAI. `NOTICE` describes how this file was made from the original.
