# KMS Knowledge Graph Assignment

Building and querying a knowledge graph of RTU study programmes using Neo4j AuraDB.

## Assignment Tasks

1. Explore the [provided dataset](https://github.com/ArithaRTU/KMS_Dataset).
2. Create a graph schema and import the data into AuraDB.
3. Run three to five queries on the knowledge graph.
4. Upload the results to this repository and submit its URL to ORTUS.

## Dataset

The dataset describes two study programmes:

- Business Informatics
- Digital Humanities

It includes study programmes, study fields, courses, topics, and learning outcomes.

## Graph Schema

The graph contains five node types:

- `StudyProgram`
- `StudyField`
- `Course`
- `Topic`
- `LearningOutcome`

### Relationships

---------------------------------------------------------
| Starting Node | Relationship        | Ending Node     |
|---------------|---------------------|-----------------|
| StudyProgram  | HAS_COURSE          | Course          |
| StudyProgram  | IN_FIELD            | StudyField      |
| Course        | HAS_TOPIC           | Topic           |
| Course        | HAS_OUTCOME         | LearningOutcome |
| StudyProgram  | HAS_PROGRAM_OUTCOME | LearningOutcome |
---------------------------------------------------------

## Queries

1. Which courses belong to Business Informatics?
2. How many distinct courses does each programme contain?
3. Which courses are shared by both programmes?
4. What are the learning outcomes of Knowledge Management Systems?
5. Which programmes and topics are connected to Knowledge Management Systems?

## Results

The report includes the graph schema, import results, and Cypher queries.
