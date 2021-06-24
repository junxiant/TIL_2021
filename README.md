# TIL_2021
DSTA's AI hackathon

For the ASR (Speech), 

1. Challenge 2: 0.97997 
2. Challenge 4: 0.78637 
3. Challenge 6: 0.49887

ASR Challenges were done with huggingface's wav2vec2 model.

1. Model trained from challenge 4 was NOT carried over to 6. (All models should be carried over) 
2. Training for challenge 4 was only based on data given for challenge 4. (ie. Not combined with challenge 2, all training data should be combined)
3. Training for challenge 4's vocab is restricted to the given training labels. (Vocab should be based on combined training data labels)
4. Training for challenge 6 was based on combined training data given for challenge 2+4+6. But is only trained on base wav2vec2 model. (Should be trained on challenge 4's model)
5. CTCBeamSearchDecocder + Language Model was only used for challenge 2/4, NOT 6. (Should be using for all challenges, Beam Search takes 1-2 hours to generate labels)
