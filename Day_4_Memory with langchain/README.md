# Day 4 

##  Topics Covered
### 1. Basic Conversation Memory
Learned how conversation history works with LLMs. Since LLMs are stateless by default, previous messages need to be stored and provided along with new user queries so that the model can maintain conversation context.
Also learned how a simple chatbot can maintain user and AI messages throughout a conversation and stop the conversation using exit commands.

---

### 2. Structured Output
Learned how to make an LLM return information in a predefined structure instead of generating only free-form text.
Structured output is useful when we need predictable and machine-readable responses from an LLM, such as extracting specific information or processing model responses programmatically.

---

### 3. Pydantic
Learned how Pydantic models can be used to define the expected structure of an LLM response.
Pydantic allows us to specify fields and their data types, such as string, integer, float, and list. This helps maintain consistent and validated structured responses.

---

### 4. Nested Pydantic Models
Learned how multiple Pydantic models can be combined to represent more complex structured data.
For example, a single movie can be represented using one model, while a list of multiple movies can be represented using another model containing a list of movie objects.
This is useful when an LLM needs to return multiple structured items in a single response.

---

## 🎯 Key Learning
Today I learned how to maintain conversation context and how to generate structured, validated, and nested outputs from LLMs using LangChain and Pydantic. 