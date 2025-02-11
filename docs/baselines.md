










## Full List of Implemented Baselines

We introduce all supported baselines and backbones.
   - `Paper`: the model name and its reference paper
   - `baseline`: the baseline name (argument `--baseline`)
	   - `ncl`: Naive Continual Learning, meaning no special continual learning is applied by default.
	   - `one`: Trains each task independently (ONE model per task)
	   - `mtl`: Trains all task together via Multi-Task Learning
   - `backbone`: the supported backbones for the corresponding baseline (argument `--backbone`)
	 - `bert`: use BERT (fine-tuning) as backbone network
	 - `bert_frozen`: use BERT (frozen) as backbone netowok (a fronzen BERT + a CNN/GRU classification network on top)
	 - `bert_adapter`: use BERT (adapter) as backbone network
	 - `w2v`: use W2V as backbone network (W2V embedding + a CNN classification network on top)
	 - `w2v_as`: use W2V as backbone network (W2V embedding which includes both review and the aspect + a CNN classificatio0n network on top)
	 - `cnn`: use CNN as backbone network (for image dataset)
	 - `mlp`: use MLP as backbone network (for image dataset)
  - `task`: the supported task for the corresponding baseline (argument `--task`)
	  - `language` dataset includes `asc/dsc/ssc/nli/newsgroup'`
	  - `image` dataset includes `celeba/femnist/vlcs/cifar10/mnist/fashionmnist/cifar100'` 




| Paper| Baseline| Backbone| task|
|--|--| -- | -- |
| NCL| ncl | bert/bert_frozen/bert_adapter/w2v_as/w2v | language,imge|
| ONE | one | bert/bert_frozen/bert_adapter/w2v_as/w2v | language,imge|
| MTL | mtl | bert/bert_frozen/bert_adapter/w2v_as/w2v | language,imge|
| L2 | l2 | bert/bert_frozen/bert_adapter/w2v_as/w2v | language,imge|
| A-GEM | a-gem | bert/bert_frozen/bert_adapter/w2v_as/w2v/cnn/mlp | language,imge|
| [DER++](https://papers.nips.cc/paper/2020/hash/b704ea2c39778f07c617f6b7ce480e9e-Abstract.html) | derpp | bert/bert_frozen/bert adapter/w2v_as/w2v/cnn/mlp | language|
| [KAN](https://www.cs.uic.edu/~liub/publications/ECML-PKDD-2020.pdf) | kan | bert_frozen/w2v_as/w2v | language|
| [SRK](https://www.cs.uic.edu/~swang/papers/lv_shared_knowledge_sentiment.pdf) | srk | bert_frozen/w2v_as/w2v | language,imge|
| EWC | ewc | bert/bert_frozen/bert_adapter/w2v_as/w2v/cnn/mlp |language,imge|
| [HAL](https://arxiv.org/abs/2002.08165) | hal | bert/bert_frozen/bert_adapter/w2v_as/w2v/cnn/mlp | language,imge|
| [UCL](https://papers.nips.cc/paper/2019/hash/2c3ddf4bf13852db711dd1901fb517fa-Abstract.html) | ucl | bert/bert_frozen/bert_adapter/w2v_as/w2v/cnn/mlp | language,imge|
| [OWM](https://www.nature.com/articles/s42256-019-0080-x) | owm | bert/bert_frozen/bert_adapter/w2v_as/w2v/cnn/mlp | language,imge|
| [ACL](https://arxiv.org/abs/2003.09553) | acl| cnn/mlp | imge|
| [HAT](http://proceedings.mlr.press/v80/serra18a.html)| hat | bert/bert_frozen/bert_adapter/w2v_as/w2v/cnn/mlp | language,imge|
| [CAT](https://proceedings.neurips.cc/paper/2020/file/d7488039246a405baf6a7cbc3613a56f-Paper.pdf)| cat | bert/bert_frozen/w2v_as/w2v/cnn/mlp| language,imge|
| [B-CL](https://aclanthology.org/2021.naacl-main.378.pdf)| b-cl|bert_adapter | language|
| [CLASSIC](https://aclanthology.org/2021.emnlp-main.550/) | classic| bert_adapter | language|
| [CTR](https://aclanthology.org/2021.emnlp-main.550/) | ctr| bert_adapter | language|



