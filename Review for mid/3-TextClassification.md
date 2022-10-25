## Text Classification ##
* Summary:
    * Input: some text x (e.g. sentence, document)
    * Output: a label y (from some finite label set)
    * Goal: learn a mapping function f from x to y
* Sentiment Analysis （作业就是）
    * Actual Task: Is the entire text of a review positive or negative?
    * 2 key components:
        * formal learning method
        * representation of the (input) data
* **Bag of Words**: Represent texts as their word counts
* **Naive Bayes**: 
    * Input Representation: Bag of words
    * Pr (𝑙𝑎𝑏𝑒𝑙|𝑡𝑒𝑥𝑡)
    * 实现的时候，long document用log会解决p太小的问题
    * unknwon的情况，用smoothing Pr(𝑤𝑖|𝑙𝑎𝑏𝑒𝑙) ≈ (𝑓(𝑤𝑖,𝑙𝑎𝑏𝑒𝑙) + 𝛼)/(𝑓(𝑤, 𝑙𝑎𝑏𝑒𝑙) + 𝛼 ∙ V)
* Evaluate Model:
    * True Table:
      | True Positive | False Positive |
      | ----------------| ------------- |
      | False Negative | True Negative |
    * Accuracy = (TP+TN)/(ALL)
    * Precision = (TP)/(TP+FP)
    * Recall = (TP)/(TP+FN)
* Improving Model:
    * Binarization: Presence of a word >>>> How many times a word occurs
    * (Log) Likelyhood Ratio