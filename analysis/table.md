

|Entity|Key Attributes|
|-|-|
|Patient|patient\_id, full\_name, date\_of\_birth, gender, blood\_group, phone, email, address, created\_at|
|Doctor|doctor\_id, full\_name, specialization, qualification, department\_id (FK), is\_head, join\_date|
|Department|department\_id, name, description, head\_doctor\_id (FK)|
|Appointment|appointment\_id, patient\_id (FK), doctor\_id (FK), scheduled\_at, status, type|
|Service|service\_id, name, type, current\_price, effective\_from|
|AppointmentService|appointment\_id (FK), service\_id (FK), quantity, unit\_price|
|MedicalRecord|record\_id, appointment\_id (FK), patient\_id (FK), doctor\_id (FK), diagnosis, treatment, created\_at|
|Bill|bill\_id, appointment\_id (FK), total\_amount, status, generated\_at|
|Payment|payment\_id, bill\_id (FK), amount, method, payment\_date|



