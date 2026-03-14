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
