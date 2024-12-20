
We're looking at how MLX differs against CUDA GPUs, so far it seems that MLX is pretty unreliable due to:

1. Memory Leaks
2. Inaccurate outputs
3. Implementation details

On the other hand, Sentence-Transformers via the mps backend's outputs are identical to the cuda implementations, and they are competitive on speed. Conservative estimate is that MLX was ~50% faster.

> Remember to set the seed when running kMeans clustering. I was seeing that Cuda and MPS embeddings were 100% identical, but downstream performance on clustering was only showing ~0.6 ARI and ~0.7 NMI, but this was due to the random seed (on a other level, it is alarming that the randoms seed has such an )