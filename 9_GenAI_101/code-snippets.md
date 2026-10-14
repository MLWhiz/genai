# Code blocks from: GenAI 101 - How Generative AI is Rewriting the Rules for ML Engineers (And How to Adapt and get Started)

Code blocks copied from the post, in order. They are fragments, not a runnable notebook.

Source: https://www.mlwhiz.com/p/genai-101-how-generative-ai-is-rewriting

## 1. Discriminative vs Generative: A 2-Minute Crash Course

```python
# APPROACH 1: Discriminative (BERT)
from transformers import BertForSequenceClassification, BertTokenizer

tokenizer = BertTokenizer.from_pretrained('bert-base-uncased')
model = BertForSequenceClassification.from_pretrained('bert-base-uncased', num_labels=2)

def predict_sentiment_discriminative(text):
    inputs = tokenizer(text, return_tensors="pt", padding=True, truncation=True)
    outputs = model(**inputs)
    return "positive" if outputs.logits[0][1] > outputs.logits[0][0] else "negative"
```

## 2. Discriminative vs Generative: A 2-Minute Crash Course

```python
# APPROACH 2: Generative (LLaMA)
from transformers import AutoModelForCausalLM, AutoTokenizer

tokenizer = AutoTokenizer.from_pretrained("meta-llama/Llama-2-7b")
model = AutoModelForCausalLM.from_pretrained("meta-llama/Llama-2-7b")

def predict_sentiment_generative(text):
    prompt = f"Review: '{text}'\nQuestion: Is this review positive or negative?\nAnswer:"
    inputs = tokenizer(prompt, return_tensors="pt")
    
    # Generate a continuation
    output = model.generate(
        inputs.input_ids, 
        max_new_tokens=5,
        temperature=0.1
    )
    
    generated_text = tokenizer.decode(output[0], skip_special_tokens=True)
    
    # Extract prediction
    prediction = generated_text.split("Answer:")[1].strip().lower()
    return "positive" if "positive" in prediction else "negative"
```

## 3. 1. Zero/Few-Shot Learning: The Cold Start Problem Solved

```python
# Scenario: Classify customer feedback without labeled examples

categories = ["shipping issue", "product quality", "billing problem", "product availability"]
new_feedback = "I was charged twice for my order but only received one package."

# APPROACH 1: Traditional ML (Discriminative)
# Without labeled examples, we simply cannot train this model
clf = RandomForestClassifier()
# clf.fit(???, ???)  # No way to train without labeled data!

# APPROACH 2: Generative AI
def classify_text(text, categories):
    prompt = f"""
    Classify the following text into exactly one of these categories: {', '.join(categories)}.
    
    Text: "{text}"
    
    The category is:
    """
    
    # API call to an LLM
    response = call_llm_api(prompt)
    return response
```

## 4. 1. Prototype in Days, Not Months

```
# Step 1: Write a prompt  
# Step 2: Ship it 🚢  
```

## 5. 3. API-Driven Dev (Goodbye, GPU Hell)

```python
import openai  
response = openai.ChatCompletion.create(...)  # Profit 💸  
```

## 6. 2. Retrieval-Augmented Generation (RAG): Your Hallucination Antidote

```python
def rag_answer(question):  
    # Step 1: Retrieve  
    relevant_text = semantic_search_knowledge_base(question)  
    # Step 2: Ground
    return generate_answer(f"Context: {relevant_text}\nQ: {question}")  
```

## 7. 5. Fine-Tuning: Bend Generative Models to Your Will

```python
# Fine-tune with LoRA (Low-Rank Adaptation)  
from peft import LoraConfig, get_peft_model  
from transformers import AutoModelForCausalLM  

model = AutoModelForCausalLM.from_pretrained("meta-llama/Llama-2-7b")  

# Inject LoRA adapters (trains only 0.5% of params!)  
config = LoraConfig(  
    r=8,  
    lora_alpha=16,  
    target_modules=["q_proj", "v_proj"],  
    lora_dropout=0.05  
)  
model = get_peft_model(model, config)  
model.print_trainable_parameters()  # "0.5% of 7B = 35M params"  

# Train  
trainer = Trainer(  
    model=model,  
    train_dataset=dataset,  
    args=TrainingArguments(  
        per_device_train_batch_size=4,  
        gradient_accumulation_steps=2,  
        warmup_steps=100,  
        max_steps=1000,  
        learning_rate=3e-4,  
        fp16=True  
    )  
)  
trainer.train()  
```

## 8. 5. Fine-Tuning: Bend Generative Models to Your Will

```python
def generate_examples(prompt_template, n=1000):
    return [llm.generate(prompt_template) for _ in range(n)]
```
