# Experiments Fastformer and Transformer performance and time cost on Sentiment Analysis task (sst2 dataset)
+ Fastformer uses Additive attention to learn global query and key vectors, its time cost and memory cost are both *O(N.d)* respectively N is the squence length, d is the hidden dimension.
+ Transformer uses self-attention to computes dot-product between input representations at each pair of positions, its time cost and memory cost are *O(N^2.d)*.

But when I experimented: 
+ **fastformer time cost is much higher than transformer and performance is sometimes worse**.
+ **positional embedding has worse performance than positional encoding.**

The encoder architecture of both models and config are the same, I only changed the capture contextual information mechanism (additive-attention & self-attention) in `fastformer_encoder.MultiHeadFastAttention` and `transformer_encoder.MultiHeadAttention`. Can you give me an explanation? 