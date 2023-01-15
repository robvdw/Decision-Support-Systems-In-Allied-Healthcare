***********

# Decision Support Systems [DSS] in Allied Healthcare
De ontembare groei van elektronische gezondheidsdossiers (EPD) in het laatste decennium heeft een overvloed aan klinische tekst opgeleverd die veelal ongestructureerd is en onbenut blijft.  Een complicerende factor is dat EPDs in Nederlandse ziekenhuizen door slechts een [drietal softwareleveranciers](https://www.zorgvisie.nl/epd-overzicht/) wordt beheerd
. Deze monopolie positie heeft er toe geleid dat de interoperabiliteit van het EPD ---koppelen van  meerdere informatiesystemen--- nogal te wensen over laat volgens de [Nederlandse academische ziekenhuizen](https://www.skipr.nl/nieuws/ziekenhuizen-openen-in-2doc-frontale-aanval-op-chipsoft/).

Desalniettemin, deze enorme hoeveelheid klinische tekstgegevens [---Big data---](https://robfvdw.medium.com/a-generic-approach-to-data-driven-activities-d85ad558b5fa) leent zich voor informatie-extractie en text mining technieken gebaseerd op Kunstmatige Intelligentie (AI) modellen binnen het Natural Language Processing [(NLP)](https://www.ibm.com/cloud/learn/natural-language-processing) toepassingsdomein. 

Speech-to-Text [(STT)](https://azure.microsoft.com/nl-nl/products/cognitive-services/speech-to-text/#overview), [NGRAM](https://mybinder.org/v2/gh/robvdw/Decision-Support-Systems-In-Allied-Healthcare/196a8b897c8f912d7417c0063616495e3bbd77aa?urlpath=lab%2Ftree%2FNotebooks%2FNGRAM-NLTK_V01.ipynb) analysis, Named [Entity Recognition (NER)](https://demos.explosion.ai/displacy-ent?text=e%20ontembare%20groei%20van%20elektronische%20gezondheidsdossiers%20(EPD)%20in%20het%20laatste%20decennium%20heeft%20een%20overvloed%20aan%20klinische%20tekst%20opgeleverd%20die%20veelal%20ongestructureerd%20is%20en%20onbenut%20blijft.%20Een%20complicerende%20factor%20is%20dat%20EPDs%20in%20Nederlandse%20ziekenhuizen%20door%20slechts%20een%20drietal%20softwareleveranciers%20wordt%20beheerd%20.%20Deze%20monopolie%20positie%20heeft%20er%20toe%20geleid%20dat%20de%20interoperabiliteit%20van%20het%20EPD%20---koppelen%20van%20meerdere%20informatiesystemen---%20nogal%20te%20wensen%20over%20laat%20volgens%20de%20100%20%0ANederlandse%20academische%20ziekenhuizen.%0A&model=nl_core_news_sm&ents=person%2Corg%2Cgpe%2Cloc%2Cproduct%2Cnorp%2Cdate%2Cper%2Cmisc%2Clanguage%2Cevent%2Ctime%2Cmoney%2Ccardinal%2Cordinal%2Cquantity%2Cpercent%2Cwork_of_art) en Relationship Extraction (RE) zijn sleutelcomponenten van NLP informatie-extractie taken met betrekking tot het benutten van terminologiestelsels [---ontologieën---](https://nl.wikipedia.org/wiki/Ontologie_(informatica)) voor de gezondheidszorg zoals [SNOMED](https://nictiz.nl/publicaties/verborgen-kant-van-snomed/).

Voordat deze data-gedreven innovatie mogelijk wordt moet je kunnen beschikken over verzamelingen aan tekst of gesproken taal [CORPORA](https://ivdnt.org/corpora-lexica/#:~:text=Een%20corpus%20is%20een%20grote,en%20voor%20allerlei%20wetenschappelijk%20onderzoek.) die woorden bevatten met betrekking tot het gebruik van taal binnen een specifiek toepassingsdomein (vakgebied) zoals de geassocieerde gezondheidszorg in Nederland [---Klinisch Psychologen, Ergotherapeuten en Fysiotherapeuten---](https://en.wikipedia.org/wiki/Allied_Healthcare).

***********

## Domain-specific (clinical) Language models in Dutch

A major difficulty to allow for NLP of dutch clinical narratives ---free-texts--- is the lack of AI-models. A wide range of AI-models are solely available
in English. The [Huggingface Transformer framework](https://aclanthology.org/2020.emnlp-demos.6/) offers
a multitude of English [Transformer models](https://jalammar.github.io/illustrated-transformer/) and variations of Bidirectional Encoder Representations
which includes the [Transformer BERT](https://arxiv.org/abs/1810.04805). 
Notably, the Huggingface-Hub comprises the [Flair framework](https://aclanthology.org/N19-4010/) 
which offers Dutch biomedical support by means of the ["BERTje transformer model"](https://arxiv.org/abs/1912.09582). 

In conclusion, automated encoding of free-text clinical narratives using concepts from
NLP is widely performed. However, the majority of open-source NLP tools --- e.g. [SpaCY](https://spacy.io/)--- and terminological systems --- e.g. [SNOMED](https://confluence.ihtsdotools.org/)--- involved are written in the English
language [Cornet et al. (2012)](https://doi.org/10.3233/978-1-61499-101-4-245).

***********

## Research Aim: Building a Custom Corpus

This project aims [1] to share pratical knowledge about how to apply NLP techniques and [2] to create a custom, domain specific ---medical---  corpus derived from clinical naratives ---allied-healthcare medical case-studies--- through the use of data enigineering [DE](https://robfvdw.medium.com/a-generic-approach-to-data-driven-activities-d85ad558b5fa) + data science [DS](https://robfvdw.medium.com/a-generic-approach-to-data-driven-activities-d85ad558b5fa) techniques and standards such as The CRoss Industry Standard Process for Data Mining [CRISP-DM](https://www.datascience-pm.com/crisp-dm-2/). 


<img align="right" width="200" height="250" src="https://user-images.githubusercontent.com/684692/198836169-675e0b2f-a5ef-4e28-9083-d9dfef0e12ce.jpg">
<img align="right" width="200" height="250" src="https://user-images.githubusercontent.com/684692/202930422-a1612d61-fe92-40cc-aaad-0aff719b29e0.jpg">

>A corpus can be large or small, though generally they consist of dozens or even hundreds of gigabytes of data inside of thousands of documents. Corpora are collections of related documents that contain natural language. Corpora can be annotated, meaning that the text or documents are labeled with the correct responses for supervised learning algorithms (e.g., to build a filter to detect spam email), or unannotated, making them candidates for topic modeling and document clustering (e.g., to explore shifts in latent themes within messages over time).
    
The endproduct should be in the form of a wel documented digital-protocol that can be readily employed by allied healthcare processionals to perform semantic and/or pragmatic NLP-techniques such as Named Entity Recognition (NER) and Relationship Extraction (RE) on dutch clinical narratives.

That is, utimately making clinical data freely exchangeable between the various professionals within the bachelor [IVG](https://www.hogeschoolrotterdam.nl/samenwerking/instituten/instituut-voor-gezondheidszorg/contact/) and other educational or research institutes of Rotterdam University of Applied Sciences [(RUAS)](https://www.rotterdamuas.com/collaboration/).

***********

## Collaboration & Data Management

This practice-based research project focuses on improving allied heathcare by applying state-of-the-art AI technologies. It is a highly transdisciplinary collaboration between [IGV](https://www.hogeschoolrotterdam.nl/samenwerking/instituten/instituut-voor-gezondheidszorg/contact/), the [CMI Minor Data Enginering](https://www.hogeschoolrotterdam.nl/samenwerking/samenwerkingsportfolio/minor-big-data-engineering---sustainability/) and the [Prometheus Data-Lab](https://www.hogeschoolrotterdam.nl/onderzoek/lectoren/creating-010/medewerkers/rob-van-der-willigen/) of the Rotterdam University of applied Sciences [---RUAS---](https://www.rotterdamuas.com/collaboration/). Supported is geven by the RUAS [Program for AI & Ethics](https://www.hogeschoolrotterdam.nl/go/ai-en-ethiek/over-ons/#flex),  the Digital Compentence Centre (DCC) for Practice-based Research  [---DCC SURF-pilot project---](https://www.surf.nl/en/news/six-new-pilots-awarded-in-dcc-for-practice-based-research) and the RUAS Data Supported Healthcare team [---Zorgtech010 data-science unit---](https://www.hogeschoolrotterdam.nl/onderzoek/projecten-en-publicaties/zorginnovatie/zorginnovatie-met-technologie/Data-Supported-Healthcare/).

The raw data wil be stored on [Research-Drive](https://www.surf.nl/en/research-drive-securely-and-easily-store-and-share-research-data) which is a EU GDPR complient service provided by SURF A data steward is responsible for managing and creating folder structures, user access, and determining quotas. Research Drive enables the use of Jupyter Notebooks.

***********

## Natural Lanuage Processing [NLP] Defined

[Natural Language Processing (NLP)](https://www.ibm.com/cloud/learn/natural-language-processing) is a hybrid AI-discipline that is developed from [linguistics](https://en.wikipedia.org/wiki/Linguistics) and [computer science](https://en.wikipedia.org/wiki/Computer_science) to make human language intelligible to machines. 
The computers’ availability in the 1960s gave rise to NLP applications on computers known as [computational linguistics](https://en.wikipedia.org/wiki/Computational_linguistics). The structure of language is hierarchical comprising of seven levels each that contrain the use of computational linguistics. 

<br>


<div align="center">
    
    
level top-to-bottom  | Structure | refers to 
----- | ----------| --------------------------------------------------------
[1] | Phonology   | Elementary sounds
[2] | Morphology  | Elementary combinations of letters and sounds, called Morphemes
[3] | Lexical     | Individual words formed of Morphemes, called Lexemes
[4] | Syntax      | Combination of words, grammatical structure of a sentence
[5] | Semantics   | Rules used to convey meaning using the lower levels
[6] | Pragmatics  | Behavioral constraints on the use of a specific language
[7] | Discourse   | Multiple sentences together, rules about how they should relate to each other
    
</div>      

<br>

Syntactic ---[parsing](https://en.wikipedia.org/wiki/Parsing)--- and semantic ---[semiotics](https://en.wikipedia.org/wiki/Semiotics)--- analysis of text and speech to determine the meaning of a sentence. Syntax refers to the grammatical structure of a sentence, while semantics alludes to its intended meaning. By allowing computers to automatically analyze massive sets of data, NLP can find meaningful information in just milliseconds. 

 

<details>
 <summary><h3>NLP covers two application-domains NLU + NLG</h3></summary>

Natural Language Understanding [(NLU)](https://en.wikipedia.org/wiki/Natural-language_understanding): It is considerd a "Hard AI-problem". The ambiguity and creativity of human language are just two of the characteristics that make NLP a demanding area to work in. The goal is to resolve ambiguities, obtain context and understand the meaning of what's being said. In particular, it tackles the complexities of language beyond the basic sentence structure. NLU is commonly used in [text mining](https://en.wikipedia.org/wiki/Text_mining) to understand consumer attitudes. In particular, sentiment analysis enables brands to monitor their customer feedback more closely, allowing them to cluster positive and negative social media comments and track net promoter scores. NLU can also establish a relevant [ontology](https://en.wikipedia.org/wiki/Ontology_(information_science)): a data structure which specifies the relationships between words and phrases. While humans naturally do this in [conversation](https://en.wikipedia.org/wiki/Discourse_analysis), the combination of these analyses is required for a machine to understand the intended meaning of different texts.
    
Natural Language Generation [(NLG)](https://en.wikipedia.org/wiki/Natural_language_generation): While NLU focuses on computers to comprehend human language, NLG enables computers to write. Initially, NLG systems used templates to generate text. Based on some data or query, an NLG system would fill in the blank, like a game of Mad Libs. But over time, natural language generation systems have evolved with the application of hidden Markov chains, recurrent neural networks, and transformers, enabling more dynamic text generation in real time. Given an internal representation, this involves selecting the right words, forming phrases and sentences. Sentences need to ordered so that information is conveyed correctly. It produces a human language text response based on some data input. This text can also be converted into a speech format through text-to-speech services.

</details>

NLU is about both analysis and synthesis ---understanding---.  Sentiment analysis and semantic search are examples of NLU. Captioning an image or video is mainly an NLG ---generating--- task since this type of input is not "textual". Text summarization and chatbot are applications that involve both [NLU + NLG](https://www.ibm.com/blogs/watson/2020/11/nlp-vs-nlu-vs-nlg-the-differences-between-three-natural-language-processing-concepts/). NLG also encompasses text summarization capabilities that generate summaries from input documents while maintaining the integrity of the information. 

***********

### Pre-Processing of free-texts & the NLP-data Pipeline

As mentioned earlier, NLP software typically analyzes text by breaking it up into
words (tokens) and sentences. Hence, any NLP pipeline has to start with a reliable
system to split the text into sentences (sentence segmentation) and further split a sentence
into words (word tokenization). On the surface, these seem like simple tasks,
and you may wonder why they need special treatment.

<img align="right" width="200" height="250" src="https://user-images.githubusercontent.com/684692/199322588-ba077b2e-8f09-4248-9259-0b61f77c28b1.png">


>NLP software typically works at the sentence level and
expects a separation of words at the minimum. So, we need some way to split a text
into words and sentences before proceeding further in a processing pipeline. Sometimes,
we need to remove special characters and digits, and sometimes, we don’t care
whether a word is in upper or lowercase and want everything in lowercase. Many
more decisions like this are made while processing text. Such decisions are addressed
during the pre-processing step of the NLP pipeline.

***********

### NLP OPEN-SOURCE Python Tools

To harnass NLP capabilities, there are high quality open-source NLP tools available allowing developers to discover valuable insights from unstructured texts.
That is, dealing with text analysis problems like classification, word ambiguity, sentiment analysis etc.

The here shown inventory is given on state-of-the-art  ---[Python programming language based](https://www.python.org/)--- open-source natural-language processing (NLP) tools & software. These are suites of libraries, frameworks, and applications for symbolic, statistical natural-language and speech processing.


Tool | NLP tasks | Distinctive features  | Neural networks | Best for | Not suitable for                          
--------|-----------|-----------------------|-----------------|----------|-----------------
NLTK    | Classification, tokenization, stemming. tagging. parsing. semantic reasoning | Over 50 corpora Package for chatbots Multilingual support| No | Training, Education, Research | Complex projects with large datasets      
Gensim | Text similarity. text summarization, SOTA topic modeling | Scalability and high performance Unsupervised training | No | Converting words and documents into vectors| Supervised text modeling Full NLP pipeline
SpaCy  | Tokenization, CNN tagging, parsing, named entity recognition. classification, sentiment analysis | 50+ languages (Dutch) available for tokenization Easy to learn and use | Yes |Teaching and research | Business production    
Textacy | Tokenization, Part-of-Speech Tagging, Dependency Parsing | High-performance SpaCy library | No | Access and extend spaCy’s core functionality | Beginners
Stanford CoreNLP Python Interface | Tokenization, multi- wordtoken expansion. lemmatization, POS tagging, dependency parsing | Different usage models Multilingual | Yes | Fully functional NLP systems, Coreference resolution | Beginners                                 
Text Blob| POS tagging.noun phrase extraction sentiment analysis, classification, translation, spelling correction, etc. | Translation and spelling correction | No | NLP prototyping | Largescale productions § altexsoft       
PyTorch-NLP | Word2Vector Encoding, Dataset Sampling | Neural Network pre-trained Embeddings | Yes | Rapid Prototyping, Research | Beginners
AllenNLP | high-level configuration language to implement many common approaches in NLP, such as transformer experiments, multi-task training, vision+language tasks, fairness, and interpretability | Solving natural language processing tasks in PyTorch |  Yes | Experimentation | Developement has stopped
FlairNLP | Get insight from text extraction, word embedding, named entity recognition, parts of speech tagging, and text classification | Sense Disambiguation + Classification, Sentiment Analysis | No  | Supports Biomedical Datasets | Business production
Spark-NLP |  NLP-library for use with Apache Spark | Easy to scale by extending Apache Spark natively | Yes | Use of SOTA transformers such as BERT & ELMO at scale by extending Apache Spark natively | Beginners


***********

### NGRAM Code example 

```
from nltk import ngrams
sentence = input("Enter the sentence: ")
n = int(input("Enter the value of n: "))
n_grams = ngrams(sentence.split(), n)
for grams in n_grams:
    print(grams)
```

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/robvdw/Decision-Support-Systems-In-Allied-Healthcare/196a8b897c8f912d7417c0063616495e3bbd77aa?urlpath=lab%2Ftree%2FNotebooks%2FNGRAM-NLTK_V01.ipynb)

***********

## References

1. NLP reference documentation: https://miro.com/app/board/uXjVOa_6fiQ=/?share_link_id=647822840290

2. https://www.hogeschoolrotterdam.nl/contentassets/e0eaa57e3ee14863911def576f414414/kennisagenda-dsh-final.pdf

3. https://www.hogeschoolrotterdam.nl/contentassets/5bbfcb19052a4bf29b6ac82c988343e4/visie-document-data-ondersteunde-gezondheidszorg-en-innovatie-8-maart-2021-2.pdf

4. https://www.researchgate.net/publication/360808997_Decision_Support_Systems_in_nursing_allied_healthcare_Building_an_AI-based_Learning_Health_System_by_use_op_Natural_Language_Processing_Tools_Dag_van_de_Fysiotherapeut_21_MEI_2022

5. https://www.researchgate.net/publication/360933051_Creating_a_Data_Fabric_through_Easy-to-Use_Cloud_Computing_DCC_SURF-Pilot_3de-ronde_2022_Produced_by_Living-Lab_AiRA_Hub_voor_Data_Responsible_AI_Hogeschool_Rotterdam_httpswwwsurfnlennewssix-new-pilot

6. https://robfvdw.medium.com/a-generic-approach-to-data-driven-activities-d85ad558b5fa

7. https://nictiz.nl/publicaties/snomed-ct-meer-dan-een-terminologiestelsel/

8. https://www.datascience-pm.com/crisp-dm-2/

9. https://www.zorgvisie.nl/content/uploads/sites/2/2018/04/Epd-overzicht2018.pdf

10. https://www.hogeschoolrotterdam.nl/go/ai-en-ethiek/projecten/postdoc-voucher-project-rob-van-der-willigen-designing-neural-networks-through-sensory-ecology/

11. [Inventory of Tools for Dutch Clinical Language Processing, 2012](https://doi.org/10.3233/978-1-61499-101-4-245)

