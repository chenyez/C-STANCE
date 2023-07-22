# C-STANCE
This is the repository for our ACL2023 main conference paper: "C-STANCE: A Large Dataset for Chinese Zero-Shot Stance Detection".

In this work:
1. We present C-STANCE, the first large Chinese zero-shot stance detection (ZSSD) dataset. Our dataset is composed of __48,126__ annotated text-target pairs. C-STANCE is more than 2.5 times larger than the English zero-shot stance detection dataset (VAST) and more than 16 times larger than the existing Chinese stance detection dataset.

2. We include two practical yet challenging ZSSD subtasks:<br />
    __Target-based zero-shot stance detection (subtask A)__, where stance detection classifiers are evaluated using a large number of completely unseen targets.<br />
    __Domain-based zero-shot stance detection (subtask B)__, where stance detection classifiers are evaluated using a large number of unseen targets from completely new domains.

4. We consider a more diverse set of targets including both __noun phrases__ and __claims__ in C-STANCE as well as multiple targets per input text.


You can find the data in the __./c_stance_dataset__ folder for subtaskA and subtaskB.

For subtaskB, each folder represents a dataset splits where data from one left-out domain (the zero-shot domain) are used for testing, while data from the rest six domains are used for training/validation.

For subtaskB, during training/validation, please filter out rows where "In Use"==0, as these are LexsimTopics that are similar to the test targets, we don't use them to ensure zero-shot learning.

The baseline pre-trained language models that we considered in our paper are from the [CLUE benchmark](https://github.com/CLUEbenchmark/CLUE)

Please cite us:
```
@inproceedings{zhao-etal-2023-c,
    title = "{C}-{STANCE}: A Large Dataset for {C}hinese Zero-Shot Stance Detection",
    author = "Zhao, Chenye  and
      Li, Yingjie  and
      Caragea, Cornelia",
    booktitle = "Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)",
    month = jul,
    year = "2023",
    address = "Toronto, Canada",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2023.acl-long.747",
    pages = "13369--13385",
    abstract = "Zero-shot stance detection (ZSSD) aims to determine whether the author of a text is in favor of, against, or neutral toward a target that is unseen during training. Despite the growing attention on ZSSD, most recent advances in this task are limited to English and do not pay much attention to other languages such as Chinese. To support ZSSD research, in this paper, we present C-STANCE that, to our knowledge, is the first Chinese dataset for zero-shot stance detection. We introduce two challenging subtasks for ZSSD: target-based ZSSD and domain-based ZSSD. Our dataset includes both noun-phrase targets and claim targets, covering a wide range of domains. We provide a detailed description and analysis of our dataset. To establish results on C-STANCE, we report performance scores using state-of-the-art deep learning models. We publicly release our dataset and code to facilitate future research.",
}
```
