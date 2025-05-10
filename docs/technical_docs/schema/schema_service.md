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

[Annex 90018](https://www.socialsecurity.be/portail/glossaires/dmfa.nsf/be8ba64d95a2ed0ec125686200574ff5/3ec8c3acff4dffc1c1258bea003378c9?OpenDocument)

