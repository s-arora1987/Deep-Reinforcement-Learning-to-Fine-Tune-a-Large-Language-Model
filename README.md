Using Deep Reinforcement Learning to Fine Tune a Large Language Model for a Text Generation Task

Task: A large language model (GPT) is pre-trained for producing positive continuation of input incomplete sentences (movie reviews). To improve the quality of generated text, use PPO (deep RL method) to fine tune the model.

The language model (LM) GPT2 generates a continuation (response) based on an input query (incomplete review). We use a pretrained BERT classifier as 'Reward Model' to generate a scalar score / reward representing the quality of the response output from LM. In the optimisation step of PPO, we use a reference LM to make sure the responses generated from 'LM being fine tuned' do not deviate too far from the reference LM. PPO training process optimizes the weights of 'LM being fine tuned' by using process outlined in image below.

Results:
Output with batch size 4 was not satisfactory. So we increased batch size to 8. 
mean rewards (before fine tuning)   -0.061082
mean rewards (after fine tuning)     1.289818

median rewards (before fine tuning)   -0.072045
median rewards (after fine tuning)     2.105461
