rasa高层架构：
![image](https://github.com/cswangjiawei/Intelligent-Furniture/blob/master/images/rasa_arch_colour.png)  
用户指令的控制部分主要由Interpreter处理，rasa本身提供有Rasa NLU。 Rasa NLU是一种开源自然语言处理工具，用于聊天机器人中的意图分类和实体提取。NLU的职责（在本例中是Rasa）是接受一个句子或是陈述，输出一个能够被机器人使用的”意图”，“实体“和“置信度”。Rasa nlu基本上提供了一个在各种NLP和ML库之上的高层次的API来负责”意图”的分类和“实体”的提取。rasa NLU采用的库通常有MITIE、spacy+sklearn,MITIE + sklearn。比如如果采用的是spacy+sklearn,则由sklearn负责分类由spacy负责实体抽取。我们要做的就是不采用rasa提供好的api进行意图分类和实体抽取，自己实现意图分类和实体抽取。实体抽取传统的机器学习方法典型的如crf,深度学习方面目前主流的技术是bilstm-crf，分类算法传统的机器学习有朴素贝叶斯、决策树等，深度学习在分类方面目前也表现良好。在意图分类方面，目前还使用的一种方法就是基于统计的方法，可以使用对话模板实现。使用rasa作为开发框架，需要将智能家居常有的功能理清，映射成相对应的intent，并理出不同情况下对应的action,slot,entity等。  
接下来的工作：  
熟练使用rasa  
严格按照rasa的要求将智能家居常有的技能编写成文件  
使用rasa开发出两个demo
