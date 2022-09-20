# bad escape \s at position 2

该更改在[问题27030](https://github.com/python/cpython/commit/9bd85b83f66d31e39282244e455275bd9cd91bb1#diff-a0fc71db3d118bcf5fa27a2eb5d4e9c5)中引入[：由正则表达式中的`'\'`和ASCII字母组成的未知转义现在都是错误](https://github.com/python/cpython/commit/9bd85b83f66d31e39282244e455275bd9cd91bb1#diff-a0fc71db3d118bcf5fa27a2eb5d4e9c5)。

![Untitled](bad%20escape%20s%20at%20position%202%20255890e3760644efaf991f7f16b74d0d/Untitled.png)

只需尝试`import regex as re`，而不是`import re`。

![Untitled](bad%20escape%20s%20at%20position%202%20255890e3760644efaf991f7f16b74d0d/Untitled%201.png)

[Python 3.7.4: 're.error: bad escape \s at position 0'](https://stackoverflow.com/questions/58328587/python-3-7-4-re-error-bad-escape-s-at-position-0)