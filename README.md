# Russian AWD-LSTM language model

This is the AWD-LSTM language model [1] trained on a subset of the Taiga corpus [2]. It can be used with vanilla PyTorch or with fast.ai [3] to get sentence representations for downstream linguistic tasks, 
such as text classification with ULMFit [4]. 

You can download weights for the model here: https://drive.google.com/open?id=1_d4XCMMWdIZt57JJyH34bzY2gRSB7KTE

**NOTE**
This model was trained a while back with an old version of fastai. If you want to use it with a newer (v1.5x+) version, run these lines before creating a learner:

```
config = awd_lstm_lm_config.copy()
config['n_hid'] = 1150
```

## Metrics

The model was trained for 10 epochs. The total number of tokens was *208,006,138*, of which 10% were used for validation. Validation results are:

| Cross-entropy | Perplexity | Accuracy |
| -------------:|-----------:|---------:|
|          3.09 |      21.98 |     0.43 |
 
## References

1. https://arxiv.org/abs/1708.02182
2. https://tatianashavrina.github.io/taiga_site/
3. https://www.fast.ai/
4. https://arxiv.org/abs/1801.06146

## Additional links

1. Similar model trained on Wikipedia: https://github.com/ppleskov/Russian-Language-Model
