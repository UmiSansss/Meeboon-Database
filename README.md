## UserType

| Type | Description |
| --- | --- |
| customer | customer of the system |
| admin | admin of the system |

## User

| Attribute | Data Type | Description | Constraints |
| --- | --- | --- | --- |
| user_id | serial | unique identifier of user | Primary Key |
| firstname | varchar(255) | firstname of user | Not Null |
| surname | varchar(255) | surname of user | Not Null |
| phonenumber | varchar(10) | phone number of user | Not Null |
| user_type | UserType | role of the user | default(customer) |

## Appointment

| Attribute | Data Type | Description | Constraints |
| --- | --- | --- | --- |
| appointment_id | serial | id of appointment | Primary Key |
| broken_part | varchar(255) | broken parts of the car that needs to be fixed | |
| short_description | varchar(255) | short description of the appointment | |
| user_id | integer | user id of the user that created this appointment | Foreign Key, Not Null |
| car_id | integer | car id of the car that needs fixing | Foreign Key, Not Null |

## Car

| Attribute | Data Type | Description | Constraints |
| --- | --- | --- | --- |
| car_id | serial | unique identifier of car | Primary Key |
| brand | varchar(255) | the brand of the car | Not Null |
| model | varchar(255) | the model of the car | Not Null |
| owner | integer | the owner of the car | Not Null |
