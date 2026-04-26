

|Item|Classification|Reason|
|-|-|-|
|Patient|Entity|Real-world actor tracked by system|
|patient\_id|Attribute (PK)|Uniquely identifies patient|
|date\_of\_birth|Attribute|Required for age calculations|
|age|Derived Attribute|Computed from date\_of\_birth|
|doctor\_id|Attribute (PK)|Uniquely identifies doctor|
|specialization|Attribute|Describes doctor expertise|
|Department|Entity|Logical grouping of doctors|
|head\_doctor\_id|Relationship Attribute|Defines role within Department|
|Appointment|Entity|Connects Patient and Doctor|
|appointment\_id|Attribute (PK)|Unique appointment reference|
|status|Attribute|Tracks appointment state|
|Service|Entity|Represents a hospital procedure/test|
|price|Attribute|Monetary value for service|
|AppointmentService|Relationship Entity|Tracks usage and quantity of services in appointments|
|quantity|Relationship Attribute|Belongs to Appointment–Service link|
|MedicalRecord|Entity|Captures treatment details|
|diagnosis|Attribute|Stored patient condition|
|Bill|Entity|Represents hospital invoice|
|total\_amount|Derived Attribute|Calculated from AppointmentService.unit\_price × quantity|
|Payment|Entity|Represents actual money transaction|
|amount|Attribute|Value per payment|
|appointment–service|Relationship (M–M)|Services can appear in multiple appointments|
|doctor–department|Relationship (1–M)|Each doctor belongs to one department|



