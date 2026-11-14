# Third-Party Notices

This file contains licensing and source notices for third-party software, libraries, models, and data resources used by or integrated with Flama Audio.

---

## 1. Kokoro Model & Weights
- **Source:** Hexgrad Kokoro-82M (https://huggingface.co/hexgrad/Kokoro-82M)
- **Artifact Source:** Built ONNX model weights and voice binaries downloaded from thewh1teagle/kokoro-onnx releases (https://github.com/thewh1teagle/kokoro-onnx)
- **Files:** `kokoro-v1.0.int8.onnx`, `voices-v1.0.bin`, `config.json`
- **License:** Apache License 2.0 (Hexgrad Kokoro-82M weights & configuration).
- **Notice:**
  Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at:
  http://www.apache.org/licenses/LICENSE-2.0

---

## 2. kokoro-onnx (C# Tooling context)
- **Source:** thewh1teagle/kokoro-onnx (https://github.com/thewh1teagle/kokoro-onnx)
- **License:** MIT License
- **Notice:**
  Copyright (c) 2024 thewh1teagle
  Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software.

---

## 3. Microsoft.ML.OnnxRuntime
- **Source:** Microsoft ONNX Runtime (https://github.com/microsoft/onnxruntime)
- **License:** MIT License
- **Notice:**
  Copyright (c) Microsoft Corporation. All rights reserved.
  Licensed under the MIT License.

---

## 4. CMUdict (Carnegie Mellon Pronouncing Dictionary)
- **Source:** cmusphinx/cmudict (https://github.com/cmusphinx/cmudict)
- **License:** Permissive BSD-style License
- **Notice:**
  Copyright (C) 1993-2015 Carnegie Mellon University. All rights reserved.

  Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

  1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
  2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

  THIS SOFTWARE IS PROVIDED BY CARNEGIE MELLON UNIVERSITY ``AS IS'' AND ANY EXPRESSED OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL CARNEGIE MELLON UNIVERSITY NOR ITS EMPLOYEES BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

---

## 5. VOICEVOX
- **Source:** VOICEVOX (https://voicevox.hiroshiba.jp/)
- **License/Terms:** 
  - The VOICEVOX Engine source code is licensed under the LGPL-3.0 License / Alternative Commercial License (https://github.com/VOICEVOX/voicevox_engine).
  - The VOICEVOX application and generated voice audio are subject to the official VOICEVOX Terms of Use.
  - Individual voice libraries/characters (e.g., Zundamon, Shikitsuren, etc.) have their own specific terms of use that must be complied with.
- **Notice:**
  Flama Audio does not bundle or claim ownership of VOICEVOX. VOICEVOX Engine and VOICEVOX applications are downloaded, hosted, and run separately by the user.

---

## 6. pinyin_dict.txt
- **Path:** `flama-audio/src/Flama.Audio.Engine.Kokoro/G2P/pinyin_dict.txt`
- **Source:** Generated during G2P development using the Python `pypinyin` package (https://github.com/mozillazg/python-pinyin).
- **Status:** **`License/source requires verification before public distribution.`** (RELEASE BLOCKER)
- **Recommendation:** 
  Before public production distribution, verify if the internal data derived from `pypinyin` allows commercial redistribution under its MIT license. If there is any ambiguity, replace or regenerate this dictionary from a fully open-source dataset with verified provenance (such as the Unicode Consortium Unihan database or CC-CEDICT).

---

## 7. misaki English lexicons (bundled in Flama.G2P)
- **Source:** hexgrad/misaki (https://github.com/hexgrad/misaki), commit `fba1236595f2d2bf21d414ba6e57d25256afada3`
- **Files:** `us_gold.json`, `us_silver.json`, `gb_gold.json`, `gb_silver.json`, embedded gzip-compressed in `Flama.G2P.dll`; the English G2P logic is ported from `misaki/en.py`.
- **License:** Apache License 2.0 (http://www.apache.org/licenses/LICENSE-2.0). Copyright hexgrad and misaki contributors.
- **Details:** See `src/Flama.Audio.Engine.Kokoro/G2P/THIRD_PARTY_NOTICES.md` for checksums and the list of changes.

---

## 8. g2p_en neural model (bundled in Flama.G2P)
- **Source:** Kyubyong/g2p (https://github.com/Kyubyong/g2p), commit `c6439c274c42b9724a7fee1dc07ca6a4c68a0538`
- **Files:** `checkpoint20.npz` (GRU weights), embedded unmodified in `Flama.G2P.dll`; inference is re-implemented in C#.
- **License:** Apache License 2.0 (http://www.apache.org/licenses/LICENSE-2.0). Copyright Kyubyong Park and Jongseok Kim.
