# SmartBenchmark
In recent years, a significant number of question answering (QA) systems that retrieve answers to natural language questions from knowledge graphs (KG) have been introduced. However, finding a benchmark to appropriately measure the quality of a question answering system is a difficult task because of (1) the high degree of variation with respect to the fine-grained properties among the available benchmarks; (2) the available benchmarks are static by nature while the KG evolving over time; (3) the existing benchmarks in the literature target only a handful of KGs. We introduce SmartBench, an on-the-fly benchmarking system for QA over KGs systems that can be used to build a QA benchmark over any KG. The benchmark generated by SmartBench is guaranteed to cover all the properties of the natural language questions and queries that were encountered in the literature as long as the targeted KG’s topology demonstrates these properties. Moreover, SmartBench generates benchmarks that follow the same standards and complexity distribution to solve the variation of the fine-grained properties among generated benchmarks.

* The web verion is available [here]( https://github.com/aorogat/SmartBenchmarkWebInterface)
* Talk: [https://www.youtube.com/toPublish](https://www.youtube.com/toDo)
* Demo talk: [https://www.youtube.com/toPublish](https://www.youtube.com/toDo)

### Features
* __Standardized:__ We propose a list of standards that need to be met in a benchmark to accurately evaluate a QA system to solve the Variations problem.
* __On-The-Fly:__  We make the benchmark generation process to be on-the-fly to avoid the Staleness issue. The system builds a new benchmark from the KG just before the evaluation process to guarantee adaptability to the evolving KG.
* __Systematic:__ Generate complex questions from simple facts in a systematic way (for generalization and scalability).
* __Richness:__ Generated questions vary in word choice (lexicon) and morphology and syntax (grammar) to evaluate the system’s ability to understand the same question written in different ways.
* __Coverability:__ We defined the question complexity to use it in tuning SmartBench to cover all possible complexities in real-world deployment. 

*Paper*: [ToPublish](https://)
#### Citation (Research Paper)
```
@Article{Orogat2022SmartBench,
  Title                    = {},
  Author                   = {},
  Journal                  = {},
  Year                     = {},
  volume                   = {},
  number                    = {}
}
```

#### Citation (Demo Paper)
```
@Article{Orogat2022demo,
  Title   = {{S}mart{B}ench: {D}emonstrating {A}utomatic {G}eneration of
{C}omprehensive {B}enchmarks for {Q}uestion {A}nswering {O}ver {K}nowledge {G}raphs},
  Author   = {Orogat, Abdelghny and El-Roby, Ahmed},
  Journal   = {Proceedings of the VLDB Endowment (PVLDB)},
  Year   = {2022},
  volume   = {15},
  number   = {12}
}
```

## Table of Content
* Run CBench
  * Getting Started
  * [Lexicon Generation](https://github.com/ToDo)
  * [Benchmark Generation](https://github.com/ToDo)
    * [DBpedia](https://github.com/aorogat/SmartBench/tree/main/benchmarks/DBpedia)
    * [Wikidata](https://github.com/ToDo)
    * [GeoLinkedData](https://github.com/aorogat/SmartBench/tree/main/benchmarks/LinkedGeoData)
    * [MAKG](https://github.com/aorogat/SmartBench/tree/main/benchmarks/MAKG)
    * [Nobel Prize](https://github.com/aorogat/SmartBench/tree/main/benchmarks/Nobel%20Prize)
  * [Benchmark Fine-Grained Analysis](https://github.com/ToDo)
  * [QA Evaluatioe](https://github.com/ToDo)


## Getting Started

### Prerequisites
SmartBench requires the following development kits and liberaries. You can download the liberaries with the system.
* for Java [JDK 8, Download liberaries as defined in the `pom` file, use Maven for this purpose.]
* You have to run the server written in Python before running the Java code. This server is in the `main.py` file and the Prerequisites for this python file can be found in the `requirements.txt` file.
* You need to install PostgreSQL 13 and create an empty database for your KG. Please reset the database paramaters from the `settings` package.

### Deploy CBench via jar
* __Download CBench.jar:__ Download the *CBench.jar* file and other folders. The project structure must be as follow
```
projectFolder
│   
└─── SmartBench.jar
│
|─── data
│   |─── benchmark.json
│   |─── src
│       │─── 
│       └─── 
│
└─── lib
    └─── ... All .jar files


```
*  __Run CBench.jar:__ Using the command ``` java -jar "PATH/TO/projectFolder/SmartBench.jar" ```, run the project.
* __Configure the System:__ While the system is running, it asks you about some parameters. Theses parameters are
  * __KG's name:__ KG name as you prefer.
  * __KG's URL:__ The URL of SPARQL endpoint of the desired knowledge graph.


## Support
Please raise potential bugs on github. If you have a research related question, please send it to this email(abdelghny.orogat@carleton.ca)



