# Metrics Glossary

## Precision

Precision measures how many of the returned results are actually relevant. It matters when users need the first few outputs to be highly useful.

## Recall

Recall measures how many of the truly relevant results were found by the system. It matters when missing a good result is costly to the user or the business.

## F1 Score

F1 score balances precision and recall into a single measure. It is useful when both irrelevant results and missed relevant results matter.

## BERTScore

BERTScore is a semantic similarity metric that compares meaning rather than exact wording. It is useful when multiple correct outputs can be phrased differently.

## BLEU

BLEU measures overlap between generated text and a reference output. It is more common in text generation research than in modern product quality evaluation, but it may still be useful in narrow cases.

## ROUGE

ROUGE measures overlap between generated and reference text with emphasis on recall. It is often used in summarization evaluation.

## Task Success Rate

Task success rate measures whether the user can complete the intended job with the output they received. In product settings, this is often more meaningful than a purely academic quality score.

## Latency

Latency measures how long it takes for the system to respond. Median latency reflects normal experience, while p95 and p99 latency reveal whether tail behavior is hurting users.

## Hallucination Rate

Hallucination rate captures how often the model produces unsupported or fabricated content. In product settings, even a low hallucination rate can have outsized trust consequences.

## User Satisfaction Score

User satisfaction score reflects direct or indirect user approval, such as thumbs up, rating, or survey response. It is useful when paired with harder operational and business metrics.

## Error Rate

Error rate measures how often the system fails technically or returns unusable results. It should include both infrastructure failures and product level failure states.

## Fallback Rate

Fallback rate measures how often the system has to revert to a simpler baseline or safe default. A high fallback rate may indicate instability, quality weakness, or an overly strict risk posture.
