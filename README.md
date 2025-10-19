# CS-499- Professional Self-Assessment



Throughout my three years in the Computer Science program, I have developed a strong foundation in programming, software design, data structures, algorithms, database management, and cybersecurity principles. Completing my coursework and developing my ePortfolio has allowed me to integrate these skills into real-world applications while showcasing my technical strengths, problem-solving abilities, and readiness to enter the professional field as a software engineer. The process of enhancing my projects and reflecting on them has also shaped my professional values of collaboration, continuous learning, and ethical responsibility in technology.

One of the most valuable experiences in this program was learning how to collaborate effectively in a team environment. In several courses I participated in team-based projects that simulated real-world development processes. I learned to use Agile methods, version control systems like GitHub, and tools such as Jira to communicate progress and manage tasks collaboratively. Working in these teams taught me the importance of version tracking, clear documentation, and regular communication to avoid conflicts in shared codebases. These experiences strengthened my teamwork and leadership abilities and prepared me for cross-functional collaboration in a professional software development setting.

Communication has also been a central theme of my growth. Through project proposals, design documents, and technical presentations, I learned how to communicate complex computing concepts clearly to both technical and non-technical stakeholders. In Software Design and Development and Mobile Architecture and Programming (CS 360), for instance, I practiced presenting design diagrams and explaining code logic to instructors and peers. These opportunities helped me refine my ability to translate technical details into understandable terms, a skill that is vital when gathering user requirements, writing documentation, or presenting solutions to management and clients in a professional role.


Security became a more prominent focus later in the program. I learned to recognize potential vulnerabilities, such as SQL injection and insecure data handling, and apply mitigations such as input validation, password hashing, and secure database connections. This awareness carried into my capstone enhancements, where I implemented SHA-256 hashing for password protection and refactored the database architecture to minimize risk. Understanding the security implications of software design decisions has reinforced my commitment to ethical and responsible coding practices—essential traits for any professional in computer science today.

Collectively, the skills I have gained across these domains—collaboration, communication, algorithms, software engineering, database management, and security—form the foundation of my professional identity. The artifacts included in my ePortfolio, particularly the enhanced *Weight Tracker mobile application*, serve as evidence of how these abilities come together in practice. The app demonstrates my ability to design modular and scalable software, apply algorithmic logic for efficiency, and integrate secure database systems—all within a real-world development environment. Together, these artifacts reflect my growth from a student learning fundamental programming concepts to a well-rounded developer capable of building secure, user-friendly, and efficient applications.

Overall, completing my coursework and creating my ePortfolio has allowed me to demonstrate not only my technical proficiency but also my adaptability, communication skills, and ethical awareness. These experiences have shaped my professional goals of becoming a software engineer who contributes to building reliable, secure, and innovative technology solutions. My portfolio captures the journey of that growth—highlighting my strengths, reflecting my learning, and showcasing the full range of computer science talents that I will bring to future professional opportunities.

-Category One: Software Engineering and Design
The artifact is the Weight Tracker mobile app, with particular focus on the 
MainActivity.java and main_screen.java files. These components serve as the entry 
point and main dashboard of the app, respectively. Users interact with the app to record 
daily weights, track progress toward personal goals, and manage weight targets. 
Originally, the main Activity and screen contained tightly-coupled logic, including 
database access, data calculations, dynamic UI generation, and user input handling. The 
enhancements were implemented to improve software design, maintainability, and 
scalability, reflecting professional software engineering principles. 
This artifact demonstrates my ability to enhance software design and application 
architecture in a real-world Android project. The focus of the enhancement was on 
separating responsibilities, improving UI/UX, and implementing modular, maintainable 
code. 
Key improvements include: 
1. Separation of Concerns: Business logic and database operations were moved to 
dedicated manager classes (DashboardManager, GoalManager), leaving the 
Activities focused solely on UI and navigation. 
2. Reusable Components: Dynamic table generation was refactored into 
TableHelper, reducing redundant code and ensuring consistent styling across the 
app. 
3. Input Validation: Numeric and valid input checks were added to prevent app 
crashes and improve user experience. 
4. Scalability and Modularity: The updated structure supports future multi-user 
functionality, UI redesigns, and database refactoring with minimal changes to the 
Activities. 
These changes highlight professional skills in software engineering principles, modular 
design, and user-focused application development. 
The enhancements support the following course outcomes: 
• Design and evaluate computing solutions using algorithmic and software 
engineering principles. 
• Implement innovative techniques, skills, and tools for software development. 
• Enhance user experience and usability through improved UI design and dynamic 
content handling. 
By implementing manager/helper classes, I applied MVC principles, modular design, 
and separation of concerns, reflecting professional software development practices. 
Enhancement Details 
1. MainActivity.java 
• Refactored login and authentication logic for clarity and maintainability. 
• Introduced LoginManager and PasswordValidator to validate credentials and 
prepare for multi-user support. 
• Simplified navigation to main_screen.java while keeping UI responsibilities 
separate. 
2. main_screen.java 
• Focused on UI rendering and navigation only. 
• Removed database queries and weight calculations from the Activity. 
• Delegated data fetching and calculations to DashboardManager and 
GoalManager. 
• Used TableHelper to dynamically generate weight entry rows with consistent 
styling. 
• Input dialogs validate numeric values before updating goals. 
3. Supporting Classes 
• DashboardManager: Handles fetching weight entries and computing remaining 
weight toward goals. 
• GoalManager: Updates user goals in the database and in the UserModel. 
• TableHelper: Generates and styles table rows dynamically for displaying weight 
entries. 
• WeightEntryDisplay: Data Transfer Object for passing weight data to the table 
helper. 
• LoginManager & PasswordValidator: Streamlined login validation and multi-user 
support. 
Reflection 
Enhancing this artifact was a valuable learning experience: 
1. Separation of Concerns: Refactoring logic into manager and helper classes 
improved readability, maintainability, and testability. 
2. UI/UX Awareness: Moving dynamic table generation to TableHelper ensured 
consistent user experience and allowed focus on UI improvements. 
3. Scalability Considerations: Modular design now supports future enhancements, 
including multi-user features, improved goal tracking, and UI redesigns. 
4. Challenges Overcome: Managing data consistency between the user model and 
database while updating the UI required careful centralization of logic, successfully 
addressed via manager classes. 
Through this process, I strengthened my ability to refactor code responsibly, apply 
software engineering principles, and design maintainable Android applications. 
Conclusion 
The enhanced Weight Tracker app, specifically the MainActivity and main_screen, 
demonstrates professional software engineering skills in creating scalable, 
maintainable, and user-friendly mobile applications. 
The artifact showcases proficiency in: 
• Modular design and separation of concerns 
• Reusable components for dynamic UI rendering 
• Preparing software for scalability and future multi-user functionality 
This project reflects my growth in Android development, software design, and 
application architecture.

Category Two: Algorithms and Data Structures
Reflection on Algorithms and Data Structure Enhancement 
For this milestone, I chose to enhance the Weight Tracker mobile app as my artifact for 
the Algorithms and Data Structure category of my ePortfolio. The original app allowed 
users to enter their daily weight and store it in a simple SQLite database, but it lacked 
advanced data handling and efficient algorithms for managing and displaying user records. 
My goal for this enhancement was to improve the app’s data organization, retrieval, and 
responsiveness to better showcase my skills in computer science principles. 
Artifact Description and Rationale 
The Weight Tracker app is an Android Studio project that tracks user weight entries and 
goals. Originally, the app relied primarily on sequential access of SQLite tables to store 
and retrieve records. I selected this artifact because it allowed me to demonstrate 
practical applications of data structures, algorithms, and object-oriented design while 
enhancing an existing project from prior coursework. 
Enhancements Implemented 
1. DashboardManager and TableHelper Integration 
a. Created a DashboardManager class to fetch and process weight records for 
display. 
b. Built a TableHelper class to dynamically populate a table in the main 
screen, showing weight, date, and remaining weight toward the user’s goal. 
c. This improvement uses lists and object-oriented principles to efficiently 
handle multiple user entries. 
2. GoalManager and Goal Update 
a. Implemented a GoalManager class to allow users to update their weight 
goals dynamically. 
b. The main screen now refreshes the table when the goal changes, 
demonstrating real-time data update and handling. 
3. Optimized Login Retrieval with HashMap Cache 
a. Introduced a HashMap<String, String> in LoginManager to cache user 
credentials. 
b. Login verification now occurs in O(1) average time, reducing reliance on 
SQLite lookups for every login attempt. 
c. The cache automatically updates when new users are added, maintaining 
consistency between the database and in-memory cache. 
4. Algorithmic User Experience Enhancements 
a. Implemented a prefix search algorithm (findClosestUser()) to suggest 
usernames if users mistype their login credentials, improving usability. 
b. Extended password validation and login checks to integrate with the cache 
and suggestion system, creating a smoother and more responsive login 
process. 
5. Algorithmic Enhancements in Weight Tracking 
a. Weight records are retrieved and sorted by date, improving efficiency for 
display operations. 
b. Calculations for “weight remaining” toward a goal are done on-the-fly using 
a simple algorithm that iterates over stored records. 
c. These enhancements demonstrate practical use of arrays/lists, 
HashMaps, loops, and basic calculations, reflecting competency in 
algorithmic thinking. 
Course Outcomes Demonstrated 
Through these enhancements, I demonstrated the ability to: 
• Design and evaluate computing solutions using algorithmic principles, such as 
sorting, caching, and search algorithms. 
• Use well-founded techniques and data structures (lists, HashMaps, singletons, 
and objects) to implement a functional mobile app. 
• Deliver professional-quality software by improving code structure, readability, 
maintainability, and responsiveness. 
Learning and Challenges 
During this process, I strengthened my understanding of algorithm optimization and data 
structures applied to real-world software. One challenge was ensuring the cache stayed 
synchronized with the database while avoiding duplicate entries. Another challenge was 
implementing the prefix search efficiently for user suggestions. By carefully designing 
LoginManager and the UserDB interface, I was able to overcome these issues. I also 
improved my knowledge of object-oriented design, singleton patterns, and algorithmic 
logic applied in mobile applications. 
Conclusion 
This enhancement allowed me to showcase practical skills in algorithms and data 
structures while improving an existing artifact for my ePortfolio. The project now 
demonstrates efficient data handling, dynamic display, goal tracking, and optimized 
login mechanisms, all of which reflect my growing expertise as a computer science 
professional. The artifact not only illustrates my ability to improve software functionality 
but also highlights my understanding of key programming principles that align with the 
course outcome.

Category Three: Databases
Reflection on Weight Tracker Project Enhancements 
Over the course of this project, I worked extensively on improving the database 
management, user authentication, and user interface of the Weight Tracker app. The main 
focus was on making the system more robust, secure, and maintainable, while also 
enhancing user experience. Below is a detailed reflection of the work completed: 
1. Database Enhancements 
Initially, the UserDB and WeightDB classes were functional but lacked several modern 
features and security measures. We implemented the following enhancements: 
• Singleton Pattern: 
Both UserDB and WeightDB were converted into singletons to prevent multiple 
database instances, ensuring consistent access and reducing the risk of memory 
leaks. 
• Password Security: 
User passwords were originally stored in plain text. We updated the system to use 
SHA-256 hashing for passwords. This ensures that sensitive user data is stored 
securely and improves overall security compliance. 
• Goal Management: 
Added goal tracking functionality in WeightDB with methods to add, update, and 
retrieve goals per user. This allows the app to notify users when they meet their 
weight goals. 
• User Validation: 
Replaced the old checkUserPassword method with validateUser, which returns 
the userID of a valid user. This streamlined the login process and simplified 
integration with UserModel. 
• Database Normalization: 
Users, goals, and records were separated into three tables with proper foreign key 
relationships, improving data integrity and making future features easier to 
implement. 
2. User Model Improvements 
• The UserModel class was refined as a singleton to store information about the 
currently logged-in user, including their username, goal, SMS notification 
preferences, and user ID. 
• This allows easy and consistent access to user information across different 
activities without redundant database calls. 
3. GoalManager Implementation 
• Introduced a dedicated GoalManager class to handle all goal-related operations. 
• This separates business logic from database code, making the system easier to 
maintain and scale. 
• Users can now update their goals, and the changes are directly reflected in the 
database. 
4. WeightDB Enhancements 
• Methods like getAllWeights, addEntry, removeEntry, and updateEntry were 
refined to work efficiently with UserModel. 
• Added proper error handling and closed all database cursors to prevent memory 
leaks. 
• Weight records are now retrieved in descending date order for better display in the 
UI. 
5. Edit View and UI Enhancements 
• The edit_view activity was improved to allow users to select multiple records 
and either delete or edit them efficiently. 
• Used dynamic TableLayout rows with checkboxes and listeners for selecting 
rows. 
• Edit functionality now prompts users for a new weight and updates the database in 
real-time. 
• Implemented a refresh mechanism after editing or deleting records to ensure the UI 
reflects the current database state. 
6. Weight Entry Form 
• Updated the weight_entry activity to integrate with the updated WeightDB and 
UserModel. 
• Added a date picker for user-friendly date input. 
• Added checks for empty input fields to prevent crashes and errors. 
• Integrated SMS notifications for when users reach their weight goals. 
7. Login and Authentication Improvements 
• Updated the login mechanism to use validateUser from UserDB. 
• This ensures that authentication is secure and reduces reliance on direct password 
comparisons. 
• The login flow is now consistent with the singleton UserModel approach, keeping 
the current user session intact across activities. 
8. Overall System Reflection 
• The project evolved from a basic weight tracker to a secure, modular, and user
friendly application. 
• Code readability and maintainability improved significantly due to separation of 
concerns (GoalManager, WeightDB, UserDB) and adherence to best practices 
(singleton patterns, password hashing, cursor management). 
• Future enhancements, such as analytics, charts, or push notifications, can be 
integrated seamlessly due to the improved architecture. 
Key Takeaways: 
1. Security is critical in apps dealing with personal data — password hashing and 
proper database structure are essential. 
2. Singleton patterns simplify state management in Android apps, especially for 
databases and user sessions. 
3. Separating business logic from database operations improves maintainability and 
scalability. 
4. User experience is improved by dynamic UI elements and real-time updates after 
data changes. 
5. Debugging and updating legacy code can be complex, but incremental 
improvements ensure stability.

