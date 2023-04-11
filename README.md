# Intro to hugging face and fine-tuning BERT

# Why are you here?

Before jumping into code or theory, why are you reading this? 

    A. Your manager saw "sentiment analysis" and told you to take this.  
    B. You recently got laid off and the abstract had a lot of key words that would look compelling on your resume.  
    C. You're a bored software engineer hoping to **transfer** into ai development.  
    D. Other?

Ultimately, we all follow tutorials hoping to **transfer** what we learn to a use-case we actually care about.

In ML speak, we call this **Transfer Learning**!

Your objective today is to learn how to fine-tune a deep learning model to accomplish a new task. After completing all of the exercises in this tutorial, you will have fine-tuned a model to assess the sentiment of a yelp review

Our objective is to fine-tune you. After completing all of the exercises in this tutorial, we will have fine-tuned you to the task of fine-tuning deep learning models. 

Let's take this a step further, because it's important intuition on what you're here to learn about. 

We couldn't teach you how to fine-tune a BERT model in 3 hours if you didn't have a lot of prerequisite knowledge. You know how to read, how to type, you have familiarity to some degree with coding in python and machine learning concepts. 

We are leveraging all that base knowledge you've come to us with and giving you 1 **epoch** of training over 3 hours, for you to learn this new task. 

You will not be an expert of HuggingFace, BERT or fine-tuning techniques at the end of this tutorial. Becoming an expert of these topics may take hundreds of epochs of training and we will provide you with some of our favorite tutorials and resources for your continued learning.

If, at the end of this tutorial, we gave you all the same quiz, would you all score the same? No, why? You are all different base-models. Some of you are native english speakers, some of you have a more limited english vocabulary. You all have different levels of experience with the various prerequisite topics that may hinder or help you pick up this new skill. 

So this elicits the question, "How do we choose which base model to fine-tune?" 

How do companies choose which human "base models" to fine-tune? There's an interview process. They assess and rank which candidates have the most relevant base knowledge so it won't cost so much to train them to do the specific tasks required. And there are trade-offs. 

Candidate A has 10 years of general coding experience and produced extremely efficient code during the coding interview.

Another candidate has 6 years of experience directly relevant to the task we are hiring for so, their salary expectations are significantly lower and their code was negligibly less efficient. 

There are a number of large open source models available for fine-tuning. A lot of tutorials jump past a lot of important ideation and evaluation of options phases. So we walk away with a specific skill that's hard to generalize and apply to tasks we care about. 

So before jumping into the code, we will briefly walk you through a sample "day in the life" case study.   



# Why'd you pick that model?

Project Scoping:

1. Present our business objective (increase adoption, improve customer satisfaction)  
2. Develop a hypothesis ML solution to meet our objective (Sentiment classification on yelp reviews)
3. Define success criteria of our experiment and scope of MVP model 

Conclusion: 

We've been given a business objective and ideal key results (OKR), we brainstormed hypotheses as to how we could leverage ML to meet our business objective. We selected a hypothesis to focus on. We narrowed the scope to an MVP experiment to evaluate if our app idea is actually useful and we've committed proactively to how we will track Key Performance Indicators to evaluate and verify if our app idea is helping us obtain the key results of our objective. 

Architecture scoping:
1. Evaluate if fine-tuning is appropriate for our use-case  
2. Narrow the scope to a category of base models 
   - hint we will touch more on high level landscape in part 4 (base model categories: NLP sequence modeling, generative vs vision, etc. )
3. Choose a base model to assess baseline performance  
   - high level landscape of sequence modeling base models to see where Bert is on the timeline & categorically

Conclusion:

We've decided on a technical design approach to pursue: we've evaluated if fine-tuning was appropriate, we evaluated which base models were appropriate for our use-case and we chose a base model for our initial MVP to obtain baseline results quickly. (This helps us get immediate feedback as to if our project technical design seems feasible)

#### Bert? (High Level)

#### DistilBert - Why are we fine-tuning this model instead?

DistilBERT is a small, fast, cheap and light Transformer model trained by distilling BERT base. It has 40% less parameters than bert-base-uncased, runs 60% faster while preserving over 95% of BERT's performances as measured on the GLUE language understanding benchmark.

It will be faster for us to train our model on DistilBERT. Best practice to create a model quickly to establish a baseline performance and iteratively add complexity if needed.  

#### Intro to Hugging Face

#### Fine tuning steps
- create a dataset (convert from pandas to a hugging face dataset)
- tokenize your training data with the same tokenizer used by the base model you are fine-tuning
- 

#### Alternative fine-tuning methods (high level and resources for further learning)