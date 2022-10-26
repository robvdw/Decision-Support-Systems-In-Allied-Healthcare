Blocks of Language |               |  Applications
------- | ------ | -------------
context  [meaning] |   ⇌⇌⇌⇌⇌⇌⇌⇌⇌⇌⇌   | Summarization / Topic modeling  / Sentiment Analysis
Syntax [phrases & sentences] |  ⇌⇌⇌⇌⇌⇌⇌⇌⇌⇌⇌   | Parsing / Entity Extraction / Relation Extraction
Morphenes & Lexemes [word] |  ⇌⇌⇌⇌⇌⇌⇌⇌⇌⇌⇌   | PTokenization / Word Embeddings / PoS Tagging

```mermaid
graph TD;
A[Move] -->|Define Date| B(Rent a van from the moving company);
B --> C{Pack boxes};
C -->|15 boxes| D[Livingroom];
C -->|5 boxes| E[Kitchen/Bath];
C -->|4 boxes| F[Bedroom];
```

```mermaid
classDiagram

    Human <|-- Astronaut
    Human <|-- Cosmonaut

    class Human {
         + firstname: str
         + lastname: str
         + say_hello()
    }

    class Astronaut {
      + agency: str = 'NASA'
    }

    class Cosmonaut {
      + agency: str = 'Roscosmos'
    }
```



# CHARTS + CODING

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```



```mermaid
graph TD;
    A[start] --> B{second node asking a question}
    B -->|Yes| C[OK]
    C --> D[go back]
    D --> B
    B ---->|No| E[End]
```

```
function test() {
  console.log("notice the blank line before this function?");
}
```




