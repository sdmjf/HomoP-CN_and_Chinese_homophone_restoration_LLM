# Accepted by the KnowFM workshop in ACL2025
The code includes various strategies for detecting LLMs' competence in restoring Internet Chinese Homophones, and the data comprises synthetic data from Deepseek and real cases from real-world internet scenarios (e.g., Weibo).

This paper discovers interesting behavior of LLM in utilizing phonological information (pinyin) to assist in homophone restoration:
1. The current small parameter models cannot achieve a satisfactory performance from the example of Llama3-8b and Qwen2.5-7B. But full parameter models like OpenAI o3-mini and Deepseek-R1 can obtain a 70%+ accuracy in restoration.
2. Phonological similarity, semantic meaning in homophones, and graphemic form differences can all influent LLMs' performance.
   2.1 Large models can work well using pinyin spelling, and they have a comprehensive positive restoration ability in restoration.
   2.2 Small models may be confused by the pinyin syllable, but they can use the same tone to associate original words.
   2.3 No matter whether large or small models, they can work better in homophones without original meanings conveyed by existing words.
   2.4 Language models cannot restore the different lengths of homophones and original words to a good enough performance.
3. Small models rely more on memory than large models.
4. Word frequency in restoring has a lower correlation with accuracy than pinyin pronunciation similarity.
5. Restored words are not consistent; different prompts will activate different corrected restored words.
6. Pinyin-enhanced alone prompt cannot assist in restoration. Besides, CoT cannot function well in small models, compared to few-shot learning. The MoT(few-shot + explicitly memory chain) can perform at optimal performance
   

If you are interested in our paper, you can access our paper directly: link (the paper link currently is not accessible to the public)


Citation information is coming soon
