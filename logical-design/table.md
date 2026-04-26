

|Entity|Primary Key|Candidate Keys|Relationship Type|Participation|
|-|-|-|-|-|
|Patient|patient\_id|email|1→M (Appointment)|Mandatory for Appointment|
|Doctor|doctor\_id|email, license\_no|1→M (Appointment)|Mandatory|
|Department|department\_id|name|1→M (Doctor)|Optional (doctor may exist before assignment)|
|Appointment|appointment\_id|—|M→M (Service via AppointmentService)|Mandatory (requires patient \& doctor)|
|Service|service\_id|name|M→M (Appointment)|Optional (some appointments may have none)|
|AppointmentService|(appointment\_id, service\_id)|—|Link|Mandatory for service usage tracking|
|MedicalRecord|record\_id|—|1→1 (Appointment)|Optional|
|Bill|bill\_id|—|1→M (Payment)|Mandatory (always connected to appointment)|
|Payment|payment\_id|—|Child of Bill|Optional (partial or multiple payments allowed)|



