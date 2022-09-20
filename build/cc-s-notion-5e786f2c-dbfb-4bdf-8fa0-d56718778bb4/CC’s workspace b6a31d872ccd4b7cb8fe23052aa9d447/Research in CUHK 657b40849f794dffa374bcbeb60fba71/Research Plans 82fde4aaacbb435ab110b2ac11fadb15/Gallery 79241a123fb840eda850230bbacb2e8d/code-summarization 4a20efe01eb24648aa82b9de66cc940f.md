# code-summarization

Created: September 14, 2022 3:32 PM

[Advances in Code Summarization](https://www.youtube.com/watch?v=-PtA0dhdsiA)

the characteristics of the summary:

- correctness
- complete: cover salient aspects of the code
- consistent: format
- fluent: easily understandable

## Need for code summarization:

- during maintenance of software, takes a a lot of time to understand the code
- frequently, developers handle code written by others
- comments don’t stay updated
- save time in writting comments\program comprehension\code search

### what about interactive comment?

when developers are writting code, AI generate template for developers to fill in some variable to form a good and clean comment?

## there are lots of abbreviations in var/functions’ name that are clear to the writters but confused to the readers

### code summarization approaches:

- Term-based
- Template-based
- external description based：correctness&quality is highly dependent on the community

![Untitled](code-summarization%204a20efe01eb24648aa82b9de66cc940f/Untitled.png)

- ML based:
    - RNN,LSTM

应用：gitcomment，comment开源，提供多种版本的comment

What’s better, an incremental adaptive natural language summarization system for source code may be designed, which will automatically improve its performance after analyzing users’ coding behavior.

有没有可能可以自动生成commit message？？？

函数名称纠正/推荐

如何从源头解决混合日志分析的问题？

公司具有统一的logging规范

where to log and what to log

tudy the repetitive usage of certain n-grams (i.e., a sequence of n tokens), which we call n-gram patterns, in the natural language descriptions.

## automated logging description

capture repetitiveness 

use the logging description in the searched code snippet as the description for current logging statement.

similarity is measured by Levenshtein distance [4], which regards a code snippet as a string and calculate the distance using character-based edit distance

use 10-fold cross vali- dation.

## Evaluation Metrics

### BLEU:Precision

use BLEU because it can measure the similarity between the candidate and the reference.

measures how many n-grams in the gen- erated logging statement appear in the reference, which enjoys similar sense as "precision".

### ROUGE:Recall

ROUGE [39] is like "recall", which measures how many n-grams in the reference appear in the generated logging statement.

![Untitled](code-summarization%204a20efe01eb24648aa82b9de66cc940f/Untitled%201.png)

5 Java projects and 3 projects, which are selected based on the number of logging descriptions.

BLEU-1 score on CoreFx is 68.76, which means that 68.76% of the tokens in the generated logging descriptions can be found in the ground truth.

The BLEU scores gradually decrease as the n-grams become longer.

For example, the BLEU-1 score on Hadoop Pre-10 is 36.59, while the corresponding BLEU-4 score is 16.96.

the BLEU scores and ROUGE scores for Java projects (Hadoop, Cloudstack, Camel, Hbase, and Hive) and C# (Mono, CoreFx, Monodevelop) are similar, which show that the effectiveness of our approach is robust against different programming languages.

gives equal weights to the edit distances of all the tokens. However, in practice, some tokens or statements are more important in this context. Thus, the performance of our model is affected.

This paper presents the first step towards automated logging de- scription generation, and thus there is no existing baseline method to compare with.

some similar tasks also generate natural language text using corresponding code snippets, such as code summarization, which aims to generate a line of text to summarize a code snippet.

The BLEU-4 scores reported in the state-of-the-art code summarization papers [31, 40] range from 6.4% to 34.3%. Meanwhile, the BLEU-4 scores of our simple information retrieval-based method range from 16.96% to 49.04% with the "Pre-10" setting, which is encouraging.