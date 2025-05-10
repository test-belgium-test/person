## Schema: Service

**Description:**  
Allows the declaration of a worker's benefits for an occupation of the worker's line. 
This schema includes several pieces of information.

### Schema Properties:

| Field Name        | Description                                                                | 
|-------------------|----------------------------------------------------------------------------|
| sequenceNbr       | Volgnummer                                                                 | 
| ServiceType       | Prestatie- of afwezigheidscode                                             | 
| startDate         | Datum of begindatum van prestatie of afwezigheid                           | 
| endDate           | Einddatum van prestatie of afwezigheid                                     | 
| nbrOfHours        | Aantal uren van prestatie of afwezigheid                                   | 

### Business Constraints:

* **Mandatory**: At least one benefit must be declared.
* **Format**: The date format is `YYYY-MM-DD` and time is expressed in hours.

### Anomalies:

Comming Soon

[Annex](https://www.socialsecurity.be/lambda/portail/glossaires/dmfa.nsf/web/glossary_home_fr)  

