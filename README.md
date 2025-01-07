# Finance-Chatbot
**Financial Conversational Chatbot with LLaMA 2 and FinGPT-fiqa_qa Dataset**

This repository contains the implementation of a financial conversational chatbot built using the LLaMA 2-7B Chat model, fine-tuned on the FinGPT-fiqa_qa dataset. The chatbot is designed to provide accurate financial advice by understanding domain-specific terminology and answering queries on market trends, investment strategies, and compliance.

**Features**
- Domain-Specific Expertise: Fine-tuned on the FinGPT-fiqa_qa dataset with 17,100 financial question-and-answer pairs, emphasizing market analysis, numerical reasoning, and contextual understanding.

- Advanced Language Model: Utilizes LLaMA 2-7B Chat, known for handling complex, multi-turn dialogues with coherence and context retention, tailored to financial advisory tasks.

- Efficient Training with PEFT and LoRA: Implements Parameter-Efficient Fine-Tuning (PEFT) and Low-Rank Adaptation (LoRA) to optimize the training process, enabling resource-efficient fine-tuning while maintaining performance.

- Interactive Financial Conversations: Equipped to respond to financial queries in a meaningful, context-aware manner, assisting underserved communities with financial literacy and decision-making.

**Dataset**

The chatbot leverages the FinGPT-fiqa_qa dataset, sourced from Hugging Face. Key features include:
- 17,100 question-answer pairs covering market analysis, investment strategies, product insights, and compliance.
- Emphasis on domain-specific jargon and real-world financial scenarios.
  
**System Architecture**
- **Dataset Preparation**

    - Data Transformation: Merged instruction, input, and output columns into a single text column for conversational training.
    - Data Splitting: 80% of data used for training, and 20% for testing, with shuffling to avoid biases.
- **Model Selection**

The project uses LLaMA 2-7B Chat, a fine-tuned variant of LLaMA-2, chosen for its:
    - Strong multi-turn dialogue handling.
    - Open-source accessibility and adaptability for domain-specific tasks.
    - Compatibility with resource-constrained environments.
- **Training Configuration**
   - Quantized Training: Reduced memory footprint using bnb_4bit quantization.
   - Fine-Tuning:
         - LoRA parameters: lora_r, lora_alpha, and lora_dropout optimized.
         - Batch size, learning rate, and gradient accumulation steps configured via Hugging Face TrainingArguments.

**Results**

The fine-tuned model demonstrated:
- Improved understanding of financial jargon and domain-specific concepts.
- Good accuracy and contextual relevance in answering financial queries.
- Scalability for real-world applications in underserved communities.
