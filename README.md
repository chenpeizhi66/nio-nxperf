# Nxperf

Nxperf is an NPU profiler I built on the chip middleware team at NIO in Shenzhen, from March 2024. It is in the style of NVIDIA Nsight Systems: a trace from operator execution down to hardware scheduling, used to find bottlenecks.

This repository is a public summary. It does not contain NIO source code, internal diagrams, customer data, or unreleased product details.

## What it covers

- A profiler lifecycle and a command-line interface with `launch` and `profile`.
- An LTTng path from collection, through parsing, to visualization.
- NPU kernel traces joined with OS scheduling, so a slow operator can be read against what the machine was doing at the same time.

## Operator work

I optimized CVA operators in CUDA with vectorized loads and stores:

- `concat`
- `im2col`
- `copy_if`
- `quantize`

On the measurements recorded for this work, inference was up to 40% faster.

## Media

Add screenshots of traces and short clips to [`media/`](media/) when they are cleared for public use. Nothing is in that folder yet.
