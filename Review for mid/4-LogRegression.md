## Logistic Regression ##
* Binary Logistic Regression 
    * Feature vector: 𝑥 = 𝑥1, 𝑥2, … , 𝑥f
    * Weights: 𝑤 = 𝑤1, 𝑤2, … , 𝑤f
    * Bias term: b
    * Use training data to learn values for weights 𝑤 and bias term b
* Logistic Regression Feature:
    * 不需要independence
* Sigmoid Function: e^z/(1+e^z)
* Multiclass Logistic Regression: 
    * Softmax Function
        * Input: vector 𝑧 = 𝑧1,𝑧2, … ,𝑧k
        * Pr(𝑦𝑘 = 1|𝑥) = (exp 𝑤𝑘 ⋅ 𝑥 + 𝑏𝑘)/sum from j = 1 to j = k(exp 𝑤𝑗⋅ 𝑥 + 𝑏j)

| Logistic regression | Naive Bayes |
| ------------------- | ----------- |
| No independence assumption | Independence assumption |
| ------------------- | ----------- |
| Weights trained jointly | Weights trained independently |
| ------------------- | ----------- |
| Better calibrated probabilities | Faster to train + Less likely to overfit |