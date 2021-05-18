# NLP_Cross_Professional_Learning

This project uses NLP abstractive summarization task to explore cross-field training and its effect on the model's capabilities. The task here is for the language model to predict a title given a body of content.

In the experiment, we trained three models using the same algorithm and based off the same pretrained BERT model:
 (1) The Star-chaser Model - a model trained solely with short movie synopsis and movie titles;
 (2) The Scholar Model - a model trained solely with the content of scientific research papers and their titles;
 (3) The Know-it-all Model -  a model trained with both training sets from (1) and (2） above.
 
After training, the following predictions are performed:
 (1) use the Star-chaser Model to predict movie titles;
 (2) use the Scholar Model to predict research paper titles;
 (3) use the Star-chaser Model to predict research paper titles;
 (4) use the Scholar Model to predict movie titles;
 (5) use the Know-it-all Model to predict movie titles;
 (6) use the Know-it-all Model to predict researachh paper titles.
 
While as expected that the Star-chaser Model performs poorly on predicting research paper titles and that the Scholar Model performs poorly on predicting movie titles, something interesting occured. The Star-chaser Model's predicted research paper titles are highly fluent while the Scholar Model's predicted movie titles often make no sense. This suggests that by learning from the movie dataset, the model acquires some kind of readibility skill. This ability is preserved in the Know-it-all Model, when using the Know-it-all model to predict research paper titles, the model predicts on par iwth the Scholar Model, witht e

This skill is preserved when applying the model to a drastically different field.
This brings some, rather than pouring datasets into the model, is there a way to train the model in a structured way with , just like how we learn in school, taking courses class by class, with each classes teaching us a focused set of skills.


The skill-specific training idea is inspired by observations from my previous paper, with only uses datasets in simplied Chinese.
[1]徐宵宁.自然语言处理之生成式短摘要预测电影片名[J].休闲,2020(24):0077-0080.

