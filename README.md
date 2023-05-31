# RDF Manipulator

This is a simple Python script used to manipulate RDF (Resource Description Framework). The script reads a CSV file containing triple data (subject, predicate, object) and adds them to an RDF graph.

## Requirements

The script relies on the following Python packages:

- csv: for reading and writing CSV files. This should be included in Python by default.
- rdflib: a Python library for working with RDF.

To install rdflib, use the following command:

```
pip install rdflib
```
It also requires an empty rdf file with a defined namespace

```
https://www.example.com/#
```

## Usage

The script expects an RDF file named `example.rdf` and a CSV file named `template.csv` in the same directory where the script is run.

### The RDF File

The RDF file should define the initial state of the graph. The graph is read and parsed at the start of the script.

### The CSV File

The CSV file should be structured with a semicolon (`;`) as the delimiter. Each row of the file represents a triple (subject, predicate, object) to be added to the graph (Refer to the template.csv). The entries in each row should correspond to identifiers in the selected namespace.

### Running the Script

After ensuring the RDF and CSV files are correctly set up, simply run the script with Python. It will read the CSV file, add all triples to the graph, and then write the updated graph back to `example.rdf` in RDF/XML format.

## Output

The script will output an RDF/XML file `example.rdf` with the updated graph.

## Note

The namespace for our resources is set to `https://doc.vayandata.com/display/LK/ontology/LinksperBuildingOntology#`. If you have a different namespace, please replace it in the script.

---

For any issues, please create a new issue in the GitHub repository. For contribution, please create a pull request.
