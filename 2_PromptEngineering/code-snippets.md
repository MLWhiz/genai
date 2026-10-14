# Code blocks from: The Art and Science of Prompt Engineering: A Comprehensive Guide

Code blocks copied from the post, in order. They are fragments, not a runnable notebook.

Source: https://www.mlwhiz.com/p/genai-series-the-art-and-science

## 1. 4. Use Examples (Few-Shot Prompting)

```
Classify these sentences as positive, neutral, or negative:

Example 1: "The food was delicious." - POSITIVE
Example 2: "The restaurant was quite crowded." - NEUTRAL
Example 3: "The service was terrible." - NEGATIVE

Now classify: "The movie had beautiful cinematography but a confusing plot."
```

## 2. 1. Zero-Shot Prompting

```
Summarize the key arguments in favor of renewable energy.
```

## 3. 2. Few-Shot Prompting

```
Convert these sentences to past tense:

Input: I walk to the store.
Output: I walked to the store.

Input: She runs every morning.
Output: She ran every morning.

Input: They build sandcastles at the beach.
Output:
```

## 4. 3. Chain-of-Thought Prompting

```
Solve this math problem step by step:
If a store sells 150 shirts at $25 each and has overhead costs of $1,500, what is the profit?
```

## 5. 5. Tree of Thoughts

```
Imagine three different experts are answering this question. All experts will write down 1 step of their thinking, then share it with the group. Then all experts will go on to the next step, etc. If any expert realises they're wrong at any point then they leave.

The question is...
There are five houses of different colors next to each other. In each house lives a man. Each man has a unique nationality, an exclusive favorite drink, a distinct favorite brand of cigarettes and keeps specific pets. Use all the clues below to fill the grid and answer the question: "Who owns the fish?"
- The Brit lives in the Red house. 
- The Swede keeps Dogs as pets. 
- The Dane drinks Tea. 
- The Green house is exactly to the left of the White house. 
- The owner of the Green house drinks Coffee. 
- The person who smokes Pall Mall rears Birds. 
- The owner of the Yellow house smokes Dunhill. 
- The man living in the centre house drinks Milk. 
- The Norwegian lives in the first house. 
- The man who smokes Blends lives next to the one who keeps Cats. 
- The man who keeps Horses lives next to the man who smokes Dunhill. 
- The man who smokes Blue Master drinks Beer. 
- The German smokes Prince. 
- The Norwegian lives next to the Blue house. 
- The man who smokes Blends has a neighbour who drinks Water.
```

## 6. 7. Step-Back Prompting

```python
Before analyzing this specific coding bug, let's step back and consider: What are the general principles of debugging memory leaks in Python applications?

[Model provides general principles of debugging memory leaks]

Now, with these principles in mind, let's examine this specific code snippet that's causing a memory leak:

```python
def process_data(data_stream):
    results = []
    for chunk in data_stream:
        processed = transform(chunk)
        results.append(processed)
    return results
```

What's likely causing the memory leak and how would you fix it?
```
