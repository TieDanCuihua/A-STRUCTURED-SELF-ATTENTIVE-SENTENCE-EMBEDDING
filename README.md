# A-STRUCTURED-SELF-ATTENTIVE-SENTENCE-EMBEDDING
《A STRUCTURED SELF-ATTENTIVE SENTENCE EMBEDDING》的学习总结
论文地址:https://arxiv.org/pdf/1703.03130.pdf。

此论文的核心思想是利用注意力机制，把一句话变成一个矩阵。此前的有很多方法是通过注意力机制把一句话变成一个向量，但论文的作者支出，一句话中有很多
信息，如果只把其变成一个向量，则只能捕获句子中的其中一个信息，为了捕获句子中的多个信息，可以把它变成一个矩阵。也就是说，我们要生成一个注意力矩阵。

为了防止此注意力矩阵重复注意句子中的某个点，论文作者提出了一个新颖的惩罚项p=||A*A_t-I||^2,A为注意力矩阵，A_t为其转置矩阵，可以想象，当A重复注意某一点时，
p会很大。

在这三个数据集the Age dataset, the Yelp dataset, and the Stanford Natural Language Inference (SNLI) Corpus中的三个任务：
author profiling, sentiment classification and textual entailment。author profiling任务是根据文章判断作者年龄，这个任务挺有意思。
其中在author profiling任务中，比一般的BiLstm提高了2.2%，在textual entailment任务中，比一般的LSTM提高了4%。详细提高请见原始论文。
