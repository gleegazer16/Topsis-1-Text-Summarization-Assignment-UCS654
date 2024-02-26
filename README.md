Text summarization is the creation of a short, accurate, and fluent summary of a longer text document. Automatic text summarization methods are greatly needed to address the ever-growing amount of text data available online. This could help to discover relevant information and to consume relevant information faster.

# Models used
model_names = [ "facebook/bart-large-cnn", "google/pegasus-large", "t5-large", "sshleifer/distilbart-cnn-12-6", "microsoft/prophetnet-large-uncased" ]

# Parameters
Evaluation Parameters used: ROGUE AND BLEU
ROGUE: Recall-Oriented Understudy for Gisting Evaluation, is a set of metrics and a software package used for evaluating automatic summarization and machine translation software in natural language processing.
BLEU: BiLingual Evaluation Understudy, is a metric for automatically evaluating machine-translated text. The BLEU score is a number between zero and one that measures the similarity of the machine-translated text to a set of high quality reference translations.
Rogue_1 -> for unigrams
Rogue_2 -> for bigrams
Rogue_l -> for longest common subsequence

 
# Analysis

Overall Model Performance:
Rouge1, Rouge2, RougeL: The evaluation results present a clear distinction in performance among the models. Model "t5-large" consistently outperforms others in capturing unigrams (ROUGE-1) and bigrams (ROUGE-2), facebook/bart-large-cnn" also performs well across all ROUGE metrics, Models "google/pegasus-large" and "microsoft/prophetnet-large-uncased" show relatively lower scores.
BLEU: All models, except "microsoft/prophetnet-large-uncased," receive extremely low BLEU scores, indicating a poor match with reference text.
TOPSIS: The TOPSIS scores reveal that "t5-large" is the top-performing model overall, followed by "facebook/bart-large-cnn" while "microsoft/prophetnet-large-uncased" receives a TOPSIS score of 0, indicating its underperformance across all metrics.

ROUGE metrics contribute significantly to the overall TOPSIS scores, emphasizing the importance of n-gram precision and recall in model ranking.
