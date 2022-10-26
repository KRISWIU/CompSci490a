## Annotation ##
* **Cohen’s Kappa**: two annotators who evaluate the same items
    * Expected probability of agreement is how often we would expect two annotators to agree assuming independent annotations
    * If classes are imbalanced, we can get higher inter annotator agreement by chance
    | na | a | b |
    | -- | -- | -- |
    | a | 7 | 4 |
    | b | 8 | 81 |
    * p_e = p(1=a,2=a) + p(1=b,2=b) 
    * k = (p_0 - p_e) / (1 - p_e)
* **Fleiss’s Kappa**:  multiple annotators, who may evaluate different items +  Each item is annotated the same number of times
    * k = (p_0 - p_e) / (1 - p_e)
    * ![Fleiss's_Kappa]()
* Krippendorff’s Alpha 信度检验
    * about real-valued labels like Likert ratings and ordinal values 处理那种没有分类的标签
    * 应该是不会考计算这个东西

* **Data**: Collection & Creation