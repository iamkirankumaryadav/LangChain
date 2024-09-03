# **LangChain** 🦜🔗 

- A Python framework that helps developers build applications that combine LLMs with other data sources and tools.
- It provides a modular and flexible way to integrate LLMs into real-world applications and leverage the power of LLMs.

### **Key components of LangChain:**
1. **Chains:** 
- These are the building blocks of **LangChain** applications.
- They define the sequence of steps that an LLM will follow to complete a task.

2. **Modules:** 
- These are reusable components that can be used in chains.
- They include modules for retrieving information from databases, searching the web, and generating text.

3. **Agents:** 
- These are autonomous entities that can interact with their environment and use LLMs to complete tasks.
- They can be used to build chatbots, virtual assistants, and other intelligent systems.

```python
from langchain.chains import LLMChain
from langchain.llms import OpenAI
from langchain.prompts import PromptTemplate
from langchain.memory import ConversationBufferMemory

# Create an LLM
llm = OpenAI(temperature=0.7)

# Create a prompt template
prompt_template = PromptTemplate(
    input_variables=["query"],
    template="Answer the following question: {query}"
)

# Create a memory:
memory = ConversationBufferMemory()

# Create a chain:
chain = LLMChain(llm=llm, prompt=prompt_template, memory=memory)

# Ask a question:
query = "What is the capital of India?"
response = chain.run(query)
print(response)
```

### **Example:**

1. When you are using **ChatGPT** as an application.
2. Internally it is making an API call to **OpenAI API**.
3. Which uses **LLMs** GPT 3.5 or GPT 4.    
