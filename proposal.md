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
2. Secure: User information is hashed in the database to secure user data. Database is encapsulated by the abstraction layer. Each part that comprises the software system is encapsulated from each other, therefore details of the individual implementations are obfuscated behind the abstraction.
3. Extensible: limitations by the database technology, in features, can be implemented through the abstraction layer. 
Application is database agnostic, therefore features requiring different persistent storage technologies for performance won't require the application team to adapt to new interfaces.
4. Maintainable: each part that comprises the software system is abstracted and encapsulated; enforcing through clearly defined lines, the design principle known as separation of concerns.

### Components
1. Client Application: provides users with movie suggestions through a graphical user interface.
2. RESTful API web service: fetches movie suggestions for the user. Saves any movie that the user wants to consider watching another time. Deletes a movie that was previously saved if the user no longer wants to save it for future consideration. Saves relevant movie data points based on user choices.
3. Persistent storage solution(s)

### Capabilities
1. Client Application is Intuive: The client application has minimal freedom of auxiliary choices behind predefined functionality. Testing coverage should be easily identifiable by the transparency of the domain.
2. RESTful API web service is extensible: The RESTful API will be stateless and its interface to the application will remain static to the agreed upon domain of initial release. As additional features of the application are added, additional interfaces will be added without concerning the application team of the particulars of how the data is being fetched and stored.
3. Client Application is maintainable: The client application's primary concern is how to effectively display the movie assets provided by the RESTful API. It's secondary concern is implementing a user movie preference algorithm and compiling it to a consistent data shape to provide the web service for saving.
4. RESTful web service is maintainable: The RESTful API will be defined by two distinct concerns. First, it's interface to the client application shall remain consistent and only changing to add additional features. Second, its implementation of the database solution(s) to accomplish the features within spec.
5. RESTful web service is secure: service validates all input to expected data shapes and calls procedures in the persistent storage solutions to obfuscate the details of the database, tables, and entities to the web service. 
6. Database is secure: the database has data hashed by the web service to obfuscate the context of the data being stored from the database and people who have access to it.

### Capabilities Count
| Component | Intuitive | Secure | Extensible | Maintainable |
|-----------|:-----------:|:-----------:|:-----------:|:-----------:|
| Application | 1 | 0 | 0 | 1 |
| Web Service | 0 | 1 | 1 | 1 |
| Database | 0 | 1 | 0 | 0 |

### Basic Testing
Unit tests to validate component capabilities are according to spec.
Integration tests to validate the correctness and performance of each software.

### Advanced Verification & Validation
End to End testing the complete software system to mimic real-world use cases.