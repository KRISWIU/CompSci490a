## Syntax: Constituency Grammars & Parsing ##
* **N-gram Language Modeling**
    * Assumption: For an ð-gram model, we approximate the conditional probability of the next word ð¤ð as follows: Pr (ð¤ð|w1:nâ1) â Pr(wN|wnâN+1:nâ1)
* Constituency Grammars
    * **Context-Free Grammar** (CFG) is used to model constituent structure https://baike.baidu.com/item/%E4%B8%8A%E4%B8%8B%E6%96%87%E6%97%A0%E5%85%B3%E6%96%87%E6%B3%95/2001908?fr=aladdin
        * å¨è®¡ç®æºç§å­¦ä¸­ï¼è¥ä¸ä¸ªå½¢å¼ææ³G = (N, Î£, P, S) çäº§çå¼è§åé½åå¦ä¸çå½¢å¼ï¼V->wï¼åè°ä¹ãå¶ä¸­ VâN ï¼wâ(NâªÎ£)* ãä¸ä¸ææ å³ææ³ååä¸ºâä¸ä¸ææ å³âçåå å°±æ¯å ä¸ºå­ç¬¦ V æ»å¯ä»¥è¢«å­ä¸² w èªç±æ¿æ¢ï¼èæ éèèå­ç¬¦ V åºç°çä¸ä¸æãä¸ä¸ªå½¢å¼è¯­è¨æ¯ä¸ä¸ææ å³çï¼å¦æå®æ¯ç±ä¸ä¸ææ å³ææ³çæçï¼æ¡ç®ä¸ä¸ææ å³è¯­è¨ï¼ã
        * A set of rules / productions of how words & symbols can be grouped
        * A lexicon of words & symbols