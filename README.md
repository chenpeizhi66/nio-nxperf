# System Profiling Tools

An NPU profiler in the style of NVIDIA Nsight Systems. It traces work from operator execution down to hardware scheduling, so a bottleneck can be read from the operator and from the machine schedule together.

This repository is a public summary. The implementation is not published here. Pictures and short videos can go in [`media/`](media/).

## What it covers

- A profiler lifecycle and a command-line interface with `launch` and `profile`.
- An LTTng path from collection, through parsing, to visualization.
- Kernel traces joined with OS scheduling.

## Operator work

These operators were rewritten in CUDA with vectorized loads and stores:

- `concat`
- `im2col`
- `copy_if`
- `quantize`

On the measurements for this work, inference was up to 40% faster.

## Media

Add screenshots of traces and short clips to `media/` and link them from this README. Nothing is in that folder yet.
