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