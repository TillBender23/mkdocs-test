# Dashboards

## EKV Dashboard

### Use Case
Dieses Dashboard stellt XYZ dar. Es besteht aus

### ETL

``` mermaid
graph LR
  A[Table1] --> |Key: Date| B{Table3};
  C[Table2] --> |Key: ID| B
  B --->|SelfJoin| B
  B --->|Result| E[Table3 in DB#Tableau];
```

#### Besonderheiten

Um die Daten aus den Tabellen X und Y zu verknüpfen wird über date und id gejoint:
``` t-sql
SELECT t.*
    FROM DB#Test t
    WHERE t.date = '2023-12-31'
    ORDER BY t.date DESC
```

## Bestellungen Dashboard

### Use Case