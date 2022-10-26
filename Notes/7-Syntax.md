## Syntax: Constituency Grammars & Parsing ##
* **N-gram Language Modeling**
    * Assumption: For an 𝑁-gram model, we approximate the conditional probability of the next word 𝑤𝑛 as follows: Pr (𝑤𝑛|w1:n−1) ≈ Pr(wN|wn−N+1:n−1)
* Constituency Grammars
    * **Context-Free Grammar** (CFG) is used to model constituent structure https://baike.baidu.com/item/%E4%B8%8A%E4%B8%8B%E6%96%87%E6%97%A0%E5%85%B3%E6%96%87%E6%B3%95/2001908?fr=aladdin
        * 在计算机科学中，若一个形式文法G = (N, Σ, P, S) 的产生式规则都取如下的形式：V->w，则谓之。其中 V∈N ，w∈(N∪Σ)* 。上下文无关文法取名为“上下文无关”的原因就是因为字符 V 总可以被字串 w 自由替换，而无需考虑字符 V 出现的上下文。一个形式语言是上下文无关的，如果它是由上下文无关文法生成的（条目上下文无关语言）。
        * A set of rules / productions of how words & symbols can be grouped
        * A lexicon of words & symbols