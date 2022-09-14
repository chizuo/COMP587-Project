# COMP 587 Project Proposal
## Contributor Names: Jonathan Chua & Chris Wheeler

### Links to SUT Source Code
- [Movie Application](https://github.com/chizuo/COMP587-Project-App)
- [RESTful API as database abstraction layer]()
- [Database Stored Procedures]()

### SUT Size
- Movie Application: *TBD*
- RESTful API web service: *TBD*
- Database Stored Procedures: *TBD*

### State of SUT
The SUT is currently in the software requirements phase. 
The software system will be developed upon approval of the proposal.

### Attributes
1. Intuitive: the application has a strict user interface to reduce unintended client actions with the rest of the system.
2. Safe: User information is hashed in the database to secure user data. Database is encapsulated by the abstraction layer.
3. Extensible: limitations by the database technology, in features, can be implemented through the abstraction layer. 
Application is database agnostic, therefore features requiring different persistent storage technologies for performance won't require the application team to adapt to new interfaces.

### Components
1. Client Application: provides users with movie suggestions through a graphical user interface.
2. RESTful API web service: fetches movie suggestions for the user. Saves any movie that the user wants to consider watching another time. Deletes a movie that was previously saved if the user no longer wants to save it for future consideration. Saves relevant movie data points based on user choices.
3. Persistent storage solution(s)

### Capabilities
1. *TBD*

### Capabilities Count
| Component | Attribute 1 | Attribute 2 | Attribute 3 | Attribute 4 |
|-----------|:-----------:|:-----------:|:-----------:|:-----------:|
| Component 1 | 0 | 0 | 0 | 0 |
| Component 2 | 0 | 0 | 0 | 0 |
| Component 3 | 0 | 0 | 0 | 0 |
| Component 4 | 0 | 0 | 0 | 0 |

### Basic Testing
Unit tests to validate component capabilities are according to spec.
Integration tests to validate the correctness and performance of each software.

### Advanced Verification & Validation
End to End testing the complete software system to mimic real-world use cases.