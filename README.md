# Maestro
In recent years, a significant number of question answering (QA) systems that retrieve answers to natural language questions from knowledge graphs (KG) have been introduced. However, finding a benchmark to appropriately measure the quality of a question answering system is a difficult task because of (1) the high degree of variation with respect to the fine-grained properties among the available benchmarks; (2) the available benchmarks are static by nature while the KG evolving over time; (3) the existing benchmarks in the literature target only a handful of KGs. We introduce Maestro, an on-the-fly benchmarking system for QA over KGs systems that can be used to build a QA benchmark over any KG. The benchmark generated by Maestro is guaranteed to cover all the properties of the natural language questions and queries that were encountered in the literature as long as the targeted KG’s topology demonstrates these properties. Moreover, Maestro generates benchmarks that follow the same standards and complexity distribution to solve the variation of the fine-grained properties among generated benchmarks.



### Features
* __Standardized:__ We propose a list of standards that need to be met in a benchmark to accurately evaluate a QA system to solve the Variations problem.
* __On-The-Fly:__  We make the benchmark generation process to be on-the-fly to avoid the Staleness issue. The system builds a new benchmark from the KG just before the evaluation process to guarantee adaptability to the evolving KG.
* __Systematic:__ Generate complex questions from simple facts in a systematic way (for generalization and scalability).
* __Richness:__ Generated questions vary in word choice (lexicon) and morphology and syntax (grammar) to evaluate the system’s ability to understand the same question written in different ways.
* __Coverability:__ We defined the question complexity to use it in tuning Maestro to cover all possible complexities in real-world deployment. 



## Table of Content
* Run Maestro
  * Getting Started
  * [Configuraion](https://github.com/aorogat/Maestro/blob/main/Configuraion.md)
  * [Lexicon Generation](https://github.com/aorogat/Maestro/blob/main/lexicon_generation.md)
  * [Benchmark Generation](https://github.com/aorogat/Maestro/blob/main/benchmark_generation.md)
    * [DBpedia](https://github.com/aorogat/Maestro/tree/main/benchmarks/DBpedia)
    * [GeoLinkedData](https://github.com/aorogat/Maestro/tree/main/benchmarks/LinkedGeoData)
    * [MAKG](https://github.com/aorogat/Maestro/tree/main/benchmarks/MAKG)
    * [Nobel Prize](https://github.com/aorogat/Maestro/tree/main/benchmarks/Nobel%20Prize)


## Getting Started

### Prerequisites
Maestro requires the following development kits and liberaries. You can download the liberaries with the system.
* for Java [JDK 8, Download liberaries as defined in the `pom` file, use Maven for this purpose.]
* You have to run the server written in Python before running the Java code. This server is in the `main.py` file and the Prerequisites for this python file can be found in the `requirements.txt` file.
* You need to install PostgreSQL 13 and create an empty database for your KG. Please reset the database paramaters from the `settings` package.

### Deploy Maestro via jar
* __Download Maestro.jar:__ Download the *Maestro.jar* file and other folders. The project structure must be as follow
```
projectFolder
│   
└─── Maestro.jar
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
*  __Run CBench.jar:__ Using the command ``` java -jar "PATH/TO/projectFolder/Maestro.jar" ```, run the project.


## Support
Please raise potential bugs on github. If you have a research related question, please send it to this email(abdelghny.orogat@carleton.ca)



