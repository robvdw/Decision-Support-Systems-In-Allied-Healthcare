# MARK DOWN DIAGRAMS

https://python.astrotech.io/design-patterns/uml/mermaid.html

https://mermaid-js.github.io/mermaid/#/theming

https://github.com/mermaidjs/mermaid-live-editor

https://support.typora.io/Draw-Diagrams-With-Markdown/

https://ckeditor.com/blog/basic-overview-of-creating-flowcharts-using-mermaid/

https://mermaid-js.github.io/mermaid-live-editor/edit#pako:eNpVj80OgkAMhF-l6UkTeQEOJgLKxUQTvbEcGqjsRvcnyxJjgHd30Yv21HS-mUxHbGzLmGLnyUm4FsJAnF2VS6_6oKmvIUm2U8kBtDX8miBblRZ6aZ1Tplt_-WyBIB-PC8YQpDL3-SvlH__J8ARFdSQXrKt_levTTrCv1FnG-H9Feo6uQ3Wj9EZJQx5y8h8EN6jZa1JtrD4uF4FBsmaBaVxb8neBwsyRoyHYy8s0mAY_8AYH11LgQlH8WGMMfvQ8vwGEfFP7

# 

Blocks of Language |               |  Applications
------- | ------ | -------------
context  [meaning] |   ⇌⇌⇌⇌⇌⇌⇌⇌⇌⇌⇌   | Summarization / Topic modeling  / Sentiment Analysis
Syntax [phrases & sentences] |  ⇌⇌⇌⇌⇌⇌⇌⇌⇌⇌⇌   | Parsing / Entity Extraction / Relation Extraction
Morphenes & Lexemes [word] |  ⇌⇌⇌⇌⇌⇌⇌⇌⇌⇌⇌   | PTokenization / Word Embeddings / PoS Tagging

#

```mermaid
flowchart RL;
    A(A)-->B(B)
```

#

```mermaid
graph TD;
A[Move] -->|Define Date| B(Rent a van from the moving company);
B --> C{Pack boxes};
C -->|15 boxes| D[Livingroom];
C -->|5 boxes| E[Kitchen/Bath];
C -->|4 boxes| F[Bedroom];
```
#

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

#

```mermaid
sequenceDiagram

    participant Client
    participant Server
    participant Database

    activate Client
    Client ->> +Server: HTTP Request
    Server ->> +Database: SQL Query
    Database -->> -Server: Result
    Server -->> -Client: HTTP Response
    deactivate Client
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
  erDiagram

    CUSTOMER }|..|{ DELIVERY-ADDRESS : has
    CUSTOMER ||--o{ ORDER : places
    CUSTOMER ||--o{ INVOICE : "liable for"
    DELIVERY-ADDRESS ||--o{ ORDER : receives
    INVOICE ||--|{ ORDER : covers
    ORDER ||--|{ ORDER-ITEM : includes
    PRODUCT-CATEGORY ||--|{ PRODUCT : contains
    PRODUCT ||--o{ ORDER-ITEM : "ordered in"
```
# 

```mermaid
graph TD;
    A[start] --> B{second node asking a question}
    B -->|Yes| C[OK]
    C --> D[go back]
    D --> B
    B ---->|No| E[End]
```
# 

```mermaid
stateDiagram-v2

        [*] --> Active

        state Active {
            [*] --> NumLockOff
            NumLockOff --> NumLockOn : EvNumLockPressed
            NumLockOn --> NumLockOff : EvNumLockPressed
            --
            [*] --> CapsLockOff
            CapsLockOff --> CapsLockOn : EvCapsLockPressed
            CapsLockOn --> CapsLockOff : EvCapsLockPressed
        }

        state SomethingElse {
          A --> B
          B --> A
        }

        Active --> SomethingElse2
        note right of SomethingElse2 : This is the note to the right.

        SomethingElse2 --> [*]
```

# 

```mermaid
gantt

    title Example Gantt diagram
    dateFormat  YYYY-MM-DD

    section Team 1
    Research & requirements :done, a1, 2000-01-01, 2000-01-20
    Review & documentation  :after a1, 2000-01-14, 20d

    section Team 2
    Implementation      :crit, active, 2000-02-01, 20d
    Testing             :crit, 20d
```

#

```mermaid
graph LR
      LB[Load Balancer] -- route1 --> web1
      LB[Load Balancer] --> web2
      web1 --> app1(fa:fa-check app1)
      web1 ==> app2
      web2 ==> app2(fa:fa-ban app2)
      web2 --> app1
      app1 --> D[(database)]
```

#

```mermaid
stateDiagram
    [*] --> Still
    Still --> [*]

    Still --> Moving
    Moving --> Still
    Moving --> Crash
    Crash --> [*]
```

#


```mermaid
pie
    title Pie Chart
    "A" : 386
    "B" : 85
    "C" : 150 
```

#

```mermaid
gitGraph
       commit
       commit
       branch develop
       checkout develop
       commit
       commit
       checkout main
       merge develop
       commit
       commit
```

#

:root {
  --mermaid-theme: default; /*or base, dark, forest, neutral, night */
  --mermaid-font-family: "trebuchet ms", verdana, arial, sans-serif;
  --mermaid-sequence-numbers: off; /* or "on", see https://mermaid-js.github.io/mermaid/#/sequenceDiagram?id=sequencenumbers*/
  --mermaid-flowchart-curve: linear /* or "basis", see https://github.com/typora/typora-issues/issues/1632*/;
  --mermaid--gantt-left-padding: 75; /* see https://github.com/typora/typora-issues/issues/1665*/
}


:root {--mermaid-theme:dark;}	Screen Shot 2020-12-05 at 17.08.46
:root {--mermaid-theme:neutral;}	Screen Shot 2020-12-05 at 17.09.42
:root {--mermaid-theme:forest;}





#

```
function test() {
  console.log("notice the blank line before this function?");
}
```




