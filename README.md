# Pizza Domain Ontology Modeling and Knowledge Graph

## Overview
This project involves creating a semantic ontology for the pizza domain using various methods and tools. The goal of this project was to model a small and general ontology for a pizza dataset to enable semantic reasoning and querying. The ontology was designed and built using **Protégé** and then extended with RDF and OWL ontologies for knowledge graph construction.

## Figure 1: Initial Ontology Modeling
In the first task, we created an initial ontology using **Protégé** for the pizza domain. This ontology was manually constructed to model key concepts within the domain, such as **restaurants** and **food**. The ontology included general concepts without any specific examples or instances. The hierarchical relationships were designed to be consistent with common standards in the field, making it compatible with other ontologies in the pizza domain.

### Key Concepts:
- **Food**: Represents different types of food, with **pizza** as one of the subclasses.
- **Restaurants**: Represents different types of eateries, such as **bars** and **caterers**.
- **Cities**, **States**, and **Countries**: Geographical attributes connected to **restaurants**.

## Building the Ontology
Various approaches were considered for building the ontology:
1. Restaurants or shops were modeled as the main entities, with relationships to other concepts.
2. A hierarchical approach was adopted, starting from **country**, then **states**, **cities**, and **restaurants**.

### Ontology Model
- **Restaurants**: Entities representing various types of eateries.
- **Food**: Including different types of pizzas (e.g., **American_pizza**, **Italian_pizza**).
- **City**, **State**, **Country**: Geographical attributes linked to **restaurants**.
- **Restaurant Types**: Such as **Bar**, **Caterer**, etc.

## Figure 3: Object and Data Properties
Object and data properties were added to define the relationships and constraints within the ontology:
- For example, some restaurants might not have postal codes, leading to cardinality constraints (0-1).
- Menus in restaurants always belong to one restaurant, but a restaurant can have multiple menus (1:*).

## Knowledge Graph Construction
In **Task 3**, we transformed the ontology into a knowledge graph:
1. The ontology from **Task 1** served as a base, guiding the extraction of triples from the dataset.
2. The triples were used to build a knowledge graph named **RDF.ttl**.
3. Popular knowledge graphs (DBpedia, Wikidata, and Google's Knowledge Graph) were utilized to extract entities related to **countries**, **cities**, and **states**.

### Queries and Results
Several SPARQL queries were written based on the knowledge graph to answer domain-related questions:
- **Query 1**: Count restaurants by city, sorted by state.
- **Query 2**: Return restaurants missing postcode values.
- **Query 3**: Calculate average price of Margherita pizza.
- **Query 4**: Retrieve restaurant details without tomato pizza.

## Aligning Ontologies
To align the newly created ontology with the Stanford Pizza Ontology:
1. The class and property lists of both ontologies were extracted.
2. Equivalent entities and semantic mappings were identified and applied using **rdflib** and **Protégé**.
3. This process helped integrate and map the concepts of both ontologies for improved interoperability.

### Results
- **Aligned Ontology**: The ontology was saved as **"Ontology_aligned_by_user.ttl"**.
- Additional alignment performed using **AML software** and **LogMap 2** provided alternative methods for mapping concepts between the ontologies.

## Files Included
- **ontology.ttl**: The initial ontology created in **Protégé**.
- **RDF.ttl**: Knowledge graph built from triples.
- **Extended_RDF.owl**: Ontology with reasoning applied.
- **Ontology_aligned_by_user.ttl**: Final aligned ontology file.
- **project_code.ipynb**: Jupyter Notebook with code for processing and analysis.

## How to Use
1. Clone the repository to your local machine.
2. Use **Protégé** for ontology exploration or analysis.
3. Execute the provided Jupyter Notebook for processing and queries against the knowledge graph.
4. Execute SPARQL queries based on your requirements.

## Acknowledgments
This project was inspired by [Stanford Pizza Ontology](https://pizza.stanford.edu/) and was designed to be compatible and extendable with other ontologies and datasets in the pizza domain.

## License
[MIT](https://opensource.org/licenses/MIT)

## Contact
- **Email**: Alirezaakhavansafaei@gmail.com
- **GitHub**: https://github.com/tifoex
- **home page**: https://studylab.ir
