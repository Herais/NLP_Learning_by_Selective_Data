# NLP_Learning_by_Selective_Data

This project uses NLP abstractive summarization task to explore cross-field training and its effect on the model's capabilities, the result sheds light to ustilizing training data selection to teach models specific skill sets.

In this experiement, BERT-based language model if finetuned to predict title given a body of context.

In the experiment, three models were trained using the same algorithm and based off the same pretrained BERT model:
 (1) The Star-chaser Model - a model trained solely with short movie synopsis and movie titles;
 (2) The Scholar Model - a model trained solely with the content of computer research papers and their titles;
 (3) The Know-it-all Model -  a model trained with both training sets from (1) and (2） above.
 
After training, the following predictions are performed:
 (1) use the Star-chaser Model to predict movie titles;
 (2) use the Scholar Model to predict research paper titles;
 (3) use the Star-chaser Model to predict research paper titles;
 (4) use the Scholar Model to predict movie titles;
 (5) use the Know-it-all Model to predict movie titles;
 (6) use the Know-it-all Model to predict researachh paper titles.
 
While as expected that the Star-chaser Model performs poorly on predicting research paper titles and that the Scholar Model performs poorly on predicting movie titles, something interesting occured. The Star-chaser Model's predicted research paper titles are highly fluent while the Scholar Model's predicted movie titles often make no sense. This suggests that by learning from the movie dataset, the model acquires some kind of readibility skill. This ability is preserved in the Know-it-all Model, when using the Know-it-all model to predict research paper titles, the model predicts on par iwth the Scholar Model, with the added benefit of fluency.

Following the observations from above, more questions are raised pertaining to training data selection,
 (1) how would the model perform if we teach it once 'class' at a time, with each class focusing on a different set of skills?
 (2) can a skill be preserved once learned and not adversely affected by continued training?


The skillset-specific training idea is inspired by observations from my previous paper, which used only simplied Chinese datasets, and performed only with prediction (1)、（2）、（4）、（5） and （6） outlined above.
[1]徐宵宁.自然语言处理之生成式短摘要预测电影片名[J].休闲,2020(24):0077-0080.


DATASETS:

1. Movie Synopsis and Title Dataset
Training:
Dev:
Test:

2. Computer Research Paper Dataset - CSL Dataset
CSL 中长文本摘要生成
https://github.com/CLUEbenchmark/CLGE#1-csl-%E4%B8%AD%E9%95%BF%E6%96%87%E6%9C%AC%E6%91%98%E8%A6%81%E7%94%9F%E6%88%90
中文科学文献数据(CSL)，选取 10k 条计算机相关领域论文及其标题作为训练集。
Download Link: https://pan.baidu.com/s/1FFG_s8z47r6e7EqoRtfIrw
Baidu Cloud Disk Code 百度网盘 提取码: u6mc
数据量：训练集(3,000)，验证集(500)，测试集(500)
Training Set 3000, Dev Set 500, Test Set 500
示例：
{
    title: 基于活跃时间分组的软件众包工人选择机制
    content: 针对现有的软件众包工人选择机制对工人间协同开发考虑不足的问题,在竞标模式的基础上提出一种基于活跃时间分组的软件众包工人选择机制。首先,基于活跃时间将众包工人划分为多个协同开发组;然后,根据组内工人开发能力和协同因子计算协同工作组权重;最后,选定权重最大的协同工作组为最优工作组,并根据模块复杂度为每个任务模块从该组内选择最适合的工人。实验结果表明,该机制相比能力优先选择方法在工人平均能力上仅有0. 57%的差距,同时因为保证了工人间的协同而使项目风险平均降低了32%,能有效指导需多人协同进行的众包软件任务的工人选择。
}
3. 


