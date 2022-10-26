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
    * Pr (𝑤𝑛|𝑤𝑛−1) ≈ (𝑓(𝑤𝑛−1|𝑤𝑛) + 𝛼)/(𝑓(𝑤𝑛−1) + 𝛼 ∙ V)


i have lunch i eat
P(i) = 2/5
p(have|i) = 1/2
P(lunch | i have) = 1
P(i have lunch) = 1/5

i, good, bad, it
pos: good, it
neg: bad, i

i like it
P(i like it | pos) = p(i|pos) * p(like|pos) * p(it|pos)
                   = p(w1|pos) * p(w2|pos) ... 
