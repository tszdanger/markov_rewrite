# Markov Speaking （马尔科夫链随机文本生成）
> This project is an package generating random sentences by markov chain. If you have any problems/ideas, please [email me](1142383654@qq.com), or open your PR. I feel honored to learn from your help.

## Platform
The `markov_speaking.py` is written in `Python 3.6`, using `jieba`, `codecs`, `random` and `re`. You need to install `jieba` by `pip2 install jieba`.

## Usage
* The `markov_speaking.py` provides a class `Markov`, the `init` of `Markov` is `__init__(self, filepath = None, mode = 0, coding="utf8")`. `filepath` is the file you want to parse, and the sentences the class build will base on this file. `mode` is 0 if you want to parse English, and 1 if Chinese. `coding` assigns the codec, default is UTF-8.
* Let `p` be a instance of `Markov`, you can use `p.train(self, filepath = '', mode = 0, coding="utf8")` to regenerate the instance.
* After you have built `p` and trained, you can use `p.say(length)` to generate a random sentence. The length is the max length of sentence to generate, default is 10.

## Examples For Use
with all the material included
```python
>>> import markov_speaking
>>> p = markov_speaking.Markov('swords.txt', 1)
Building prefix dict from the default dictionary ...
Loading model from cache /home/forec/cache
Dumping model to file cache /home/forec/cache
Loading model cost 1.578 seconds.
Prefix dict has been built succesfully.
>>> p.say(5)
忽然想到一计说道师伯令狐师兄行侠仗义。
```

## Update-logs
* 2019-5-12: change it to py3
* 2016-10-10: Add project and build repository.
* 2016-10-11: Fix problems in English part: Not split words by sentences.
* 2016-10-12: Fix train function.
* 2016-10-13: Remove useless chinese upper condition.


