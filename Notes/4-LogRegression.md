## Logistic Regression ##
* Binary Logistic Regression 
    * Feature vector: π₯ = π₯1, π₯2, β¦ , π₯f
    * Weights: π€ = π€1, π€2, β¦ , π€f
    * Bias term: b
    * Use training data to learn values for weights π€ and bias term b
* Logistic Regression Feature:
    * δΈιθ¦independence
* Sigmoid Function: e^z/(1+e^z)
* Multiclass Logistic Regression: 
    * Softmax Function
        * Input: vector π§ = π§1,π§2, β¦ ,π§k
        * Pr(π¦π = 1|π₯) = (exp π€π β π₯ + ππ)/sum from j = 1 to j = k(exp π€πβ π₯ + πj)
| Logistic regression | Naive Bayes |
| ------------------- | ----------- |
| No independence assumption | Independence assumption |
| Weights trained jointly | Weights trained independently |
| Better calibrated probabilities | Faster to train + Less likely to overfit |

* OverFitting: Penalize large weights 
    * L2 regularization: εΉ³ζΉ
    * L1 regularization: η»ε―ΉεΌ


f(x) = e^(-ax)/(1+e^(-ax))
