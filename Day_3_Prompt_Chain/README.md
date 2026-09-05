LangChain LCEL Chain with ChatGroq

A simple LangChain project demonstrating an LLM chain using LCEL.

🔗 Chain Flow
Prompt → ChatGroq → StrOutputParser → transform_case
🛠️ Technologies
Python
LangChain
LCEL
ChatGroq
GPT-OSS-20B
Code: 
from langchain_core.prompts import ChatPromptTemplate
from langchain_core.output_parsers import StrOutputParser
from langchain_groq import ChatGroq

prompts = ChatPromptTemplate.from_messages([
    ("system", "You are a translator. Translate the given text into {language}."),
    ("human", "{query}")
])

llm = ChatGroq(
    model="openai/gpt-oss-20b"
)

output_parser = StrOutputParser()

def transform_case(result):
    return result.upper()

chains = prompts | llm | output_parser | transform_case

response = chains.invoke({
    "language": "Bangla",
    "query": "I love to play cricket."
})

print(response)

Key Learnings
Prompt Templates
LCEL Pipe Operator |
ChatGroq integration
Output Parsing
Custom transformation functions
Chain execution with .invoke()