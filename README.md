# Oficina Explorando a IA: da teoria à prática 📚👐

## #MulheresNaTech - Microsoft Reactor

### Bora codar? 👩‍💻💜

<img src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExOXdxcWgxYnpvaHkxemhzMXV6cjljNmZ0bnNtZGgwOHUzdm8wNjBxMSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/6EWyszhJ2kL3ceQuD2/giphy.gif" width="300" height="300" alt="Alt Text ">

## Links úteis: 

* Open AI [https://openai.com]

* Documentação Open API [https://platform.openai.com/docs/api-reference/streaming]

* Github Codespaces  [https://github.com/codespaces]  

### Trechos de código para nos ajudar:

- Baralho:

``` python
  "The Fool", "The Magician", "The High Priestess", "The Empress", "The Emperor",
  "The Hierophant", "The Lovers", "The Chariot", "Strength", "The Hermit",
  "Wheel of Fortune", "Justice", "The Hanged Man", "Death", "Temperance",
  "The Devil", "The Tower", "The Star", "The Moon", "The Sun",
  "Judgement", "The World"
```

- Prompt
  
```python
"You are a tarot reader, and you drew cards {card1}, {card2} and {card3} "
"from the tarot deck for me. What future do you see for me? Answer me like a tarot "
"reader in portuguese."
```

- Streaming do OPENAI

```python
from openai import OpenAI

client = OpenAI(
     api_key = "minha-chave-super-secreta-aqui"
)


stream = client.chat.completions.create(
    model="gpt-3.5-turbo-0125",
    messages=[{"role": "user", "content": input}],
    stream=True,
)
for chunk in stream:
    if chunk.choices[0].delta.content is not None:
        print(chunk.choices[0].delta.content, end="")
```

- Minha chave super secreta
* Doczin

