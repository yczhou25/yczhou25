### Hi, I'm Yichuan Zhou 👋

Undergraduate in Electronic Information Engineering at the University of Electronic Science and Technology of China (UESTC), currently pursuing a master's degree in Integrated Circuits at Nanyang Technological University, Singapore. Recording my work on AI infrastructure: large model inference engine (KV cache, prefix caching, scheduling, speculative decoding) and the underlying hardware—looking forward to learning and exchanging ideas with all of you.
电子科技大学（985）电子信息工程本科，目前在新加坡南洋理工大学集成电路读硕士。记录做 AI infra：大模型推理引擎（KV cache、前缀缓存、调度、投机解码）和它下面的硬件，希望多多跟各位大佬学习交流。

#### Upstream contributions
- **[vLLM](https://github.com/vllm-project/vllm)**
  - [#59683](https://github.com/vllm-project/vllm/pull/59683) `[Bugfix][Core]` Keep the aligned sliding-window prefix-cache hit when dropping the EAGLE block (`SlidingWindowManager.find_longest_cache_hit`)
  - [#63325](https://github.com/vllm-project/vllm/pull/63325) `[Bugfix][Core]` Hash every overlapping multimodal item into prefix-cache block keys (Qwen2.5/3-Omni with `use_audio_in_video=True` could reuse another request's KV cache), validated end-to-end on GPU

#### Projects
- **[nano-vllm-spec](https://github.com/yczhou25/nano-vllm-spec)**: nano-vllm extended with **async scheduling** (CPU scheduling overlapped with GPU forward) and **speculative decoding** with n-gram and draft-model drafts, including async + draft model combined, plus two tensor-parallel bug fixes found by auditing the code. A randomized engine simulator checks every KV-cache write and read on CPU; GitHub Actions CI; A40 benchmarks in progress.
- **[mini-tpu](https://github.com/yczhou25/mini-tpu)**: a TPU-v1-style weight-stationary systolic-array accelerator in Verilog, taken from RTL to a signed-off SkyWater 130nm layout in Caravel's user area (231 MHz, DRC/LVS/antenna clean). Runs MLPs, CNNs, ResNet, a ViT and a character-level GPT on chip, bit-exact against NumPy; 2:4 sparsity and int4 weights.

#### Interests
LLM serving systems · KV cache management · speculative decoding · GPU kernels · ML accelerators
