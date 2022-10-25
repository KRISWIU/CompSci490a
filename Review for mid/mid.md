## Regular Expression ##
* Character classes
    * Disjunction of listed characters
        * [Ww ]ord = word / Word
    * Ranges
        * [A-Z ]: any upper case letter
    * Negation of class [^...... ]
    * ? * + .: 
        * ?: Optional previous char (Colou?r = Color/Colour)
        * !: 0 or more of previous char (oo!h = oh/ooooh/oooooooh)
        * +: 1 or more of previous char (o+h = oo!h)
        * .: 替代任意char
* Tokenlization
    * Stages of text processing: 1. segment text into words, 2. normalization 3. 更细节的segmentation
    * Stemming & Lemmatizing
        * Stem 就是 playing -> play (faster)
        * Lemmatizing 就是 is -> be (slower)

## Language Modeling ##
* Zipf's Law: 大概就是单词出现的频率和在频率表的排名成反比
* Language Modeling: Model the chance of a word or text occurring
    * Pr 𝑡𝑒𝑥𝑡 = Pr(𝑤1,𝑤2, … ,𝑤𝑛) ; Pr(𝑛𝑒𝑥𝑡 𝑤𝑜𝑟𝑑) = Pr(𝑤𝑛+1|𝑤1,𝑤2, … ,𝑤𝑛)
    * Chain Rule: Pr 𝑥1𝑥2𝑥3𝑥4 = Pr(𝑥1) ⋅ Pr(𝑥2|𝑥1) ⋅ Pr(𝑥3|𝑥1𝑥2) ⋅ Pr(𝑥4|𝑥1𝑥2𝑥3)
* N-gram Language Model: 
    * Simplest: Unigram Model: P(x1x2x3x4) = P(x1) ⋅ P(x2) ⋅ P(x3) ⋅ P(x4)
    * Biggram Model : P(x1x2x3x4) = P(x1) ⋅ P(𝑥2|𝑥1) ⋅ P(x3|x2) ⋅ P(x4|x3)
    * Trigram Model 
* Evaluation Language Models:
    * **Extrinsic** evaluation: Measure model quality by **application** performance
    * **Intrinsic** evaluation: Measure model quality **independent** of applications
    * Perplexity: PP(W) = (1/Pr(w1,w2,...,wn))^(1/n)
* Additive Smoothing: avoid zero probabilities
    * Pr (wi) ≈ (𝑓(𝑤𝑖) + 𝛼)/(𝑁 + 𝑉)   
    * Pr (𝑤𝑛|𝑤𝑛−1) ≈ (𝑓(𝑤𝑛−1 𝑤𝑛) + 𝛼)/(𝑓(𝑤𝑛−1) + 𝛼 ∙ V)

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
    * | True Positive | False Positive |
      | ----------------| ------------- |
      | False Negative | True Negative |