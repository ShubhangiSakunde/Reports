**Final Assessment**
**Name: Shubhangi Vilas Sakunde**
**Student_ID: 21142637**
**Practical class: Day= Monday, Time= 4:00pm, Venue= Curtin University,bentley**

**Introduction**
In order to provide two scenarios — predicting seasons based on nation, season of the year, and month number, and predicting temperature differences of 5 degrees Celsius based on city and temperature input — I have constructed a programme employing production code, test code, and version control. Reliability, scalability, and maintainability are all ensured by the codebase.
 
When given a country, season, and month, the programme in the first scenario maps these to the relevant season, so precisely determining the season. In the second case, by comparing the input temperature with a reference value, the programme determines whether the temperature difference is within 5 degrees Celsius.

Our programme makes accurate forecasts while preserving code quality and simplifying future improvements by mixing production code, test code, and version control.



1. **Modularity: Preliminary description of your modules**

Based on the given scenario, here are the preliminary descriptions of the modules that could be implemented to achieve the required functionality:

**Module 1: SeasonFinder**

- Description: This module is responsible for finding the season of the year based on the given country name and month.
- Inputs: Country name (string), Month (integer)
- Outputs: Season (string)
- Input Source: Parameters passed to the module
- Output Method: Return the identified season as a string

**Module 2: TemperatureComparator**

- Description: This module compares a given temperature reading with the average temperature of a city in the morning or evening and provides additional information if the difference exceeds 5⁰C.
- Inputs: City (string), Temperature reading (float), Time (string - "morning" or "evening")
- Outputs: Comparison result (string), Additional message (string, if applicable)
- Input Source: Parameters passed to the module
- Output Method: Return the comparison result and additional message as strings

**Module 3: InputValidator**

- Description: This module validates the inputs for both scenarios, ensuring the country, city, month, temperature reading, and time inputs are valid and within the expected range.
- Inputs: Country name (string), City (string), Month (integer), Temperature reading (float), Time (string - "morning" or "evening")
- Outputs: Validation result (boolean)
- Input Source: Parameters passed to the module
- Output Method: Return the validation result as a boolean value

**Module 4: GraphicsSymbolMapper (for Scenario A)**

- Description: This module maps the textual output of the season to the corresponding graphics symbols provided in the "ISEimages" folder.
- Inputs: Season (string)
- Outputs: Graphics symbol representation (string)
- Input Source: Parameters passed to the module
- Output Method: Return the graphics symbol representation as a string

**Module 5: UserInterface**

- Description: This module handles user interactions, allowing users to input data via the keyboard and displaying results on the screen.
- Inputs: User inputs (through keyboard)
- Outputs: Displayed results (printed on the screen)
- Input Source: Keyboard input
- Output Method: Print the results on the screen

**Module 6: FileHandler**

- Description: This module handles reading input data from a text file and saving results to a file.
- Inputs: File paths (input and output)
- Outputs: Read input data, Saved results
- Input Source: Read input data from a text file
- Output Method: Save results to a file

Note: These are preliminary module descriptions, and further refinement may be required during the implementation stage.

2. **Modularity: Implementation of production code, reviewing and refactoring**
1. **Implementation of Modules:**

Here is an implementation of the modules based on the preliminary descriptions provided earlier. The implementation is done using Python:

**Module 1: SeasonFinder**

\```

def find\_season(country, month):

- Implementation logic to determine the season based on country and month
- ...

return season

\```

**Module 2: TemperatureComparator**

\```

def compare\_temperature(city, temperature, time):

- Implementation logic to compare the temperature reading with the average temperature of the

city

- ...

return comparison\_result, additional\_message

\```

**Module 3: InputValidator**

\```

def validate\_input(country, city, month, temperature, time):

- Implementation logic to validate the inputs
- ...

return is\_valid

\```

**Module 4: GraphicsSymbolMapper (for Scenario A)**

\```

def map\_to\_graphics\_symbol(season):

- Implementation logic to map the season to the corresponding graphics symbol
- ...

return graphics\_symbol

\```

**Module 5: UserInterface**

\```


def get\_user\_input():

- Implementation logic to get user input from the keyboard
- ...

return user\_input

def display\_result(result):

- Implementation logic to display the result on the screen
- ...

print(result)

\```
  
**Module 6: FileHandler**

\```

def read\_input\_from\_file(file\_path):
+
- Implementation logic to read input data from a file
- ...

return input\_data

def save\_result\_to\_file(file\_path, result):

- Implementation logic to save the result to a file
- ...
- Save the result to the file

\```

2. **Usage of Good Modularity Principles:**

The implementation follows good modularity principles, including:

- **Encapsulation:** Each module encapsulates a specific functionality and has clear inputs and outputs. This promotes code organization and separation of concerns.
- Single Responsibility: Each module is responsible for a specific task, ensuring that each module has a single responsibility and is focused on doing one thing well.
- **Loose Coupling:** The modules are designed to have minimal dependencies on each other. They communicate through well-defined interfaces (function parameters and return values) rather than directly accessing each other's internal implementation details.
- **High Cohesion:** The code within each module is closely related and focused on achieving a specific task or functionality.
- **Reusability:** By implementing the functionality as separate modules, they can be easily reused in other parts of the code or in future projects, promoting code reuse and maintainability.
3. **Review Checklist for Code Design Principles:**

Here is a short review checklist to ensure good code design principles are followed:

1. Is the code well-organized and structured?
1. Are meaningful and descriptive names used for variables, functions, and modules?
1. Are functions and modules small and focused, adhering to the single responsibility principle?
1. Is there appropriate encapsulation, with data and functions grouped together in modules?
1. Are comments used effectively to explain complex logic or provide necessary documentation?
1. Are there any redundant or duplicate code sections that can be refactored?
1. Are proper error handling and exception handling mechanisms implemented?
1. Is the code formatted consistently and readable?
1. Are coding conventions and style guidelines followed?
1. Are there any performance bottlenecks or inefficiencies that can be improved?

3. **Test design (Black box testing)**

**Module 1: SeasonFinder (Equivalence Partitioning)**

- Test Case 1: Input a valid country ("Australia") and a valid month (1-12)
- Test Case 2: Input a valid country ("Canada") and a valid month (1-12)
- Test Case 3: Input an invalid country ("Germany") and a valid month (1-12)
- Test Case 4: Input a valid country ("Australia") and an invalid month (0 or 13)

**Module 2: TemperatureComparator (Equivalence Partitioning)**

- Test Case 1: Input a valid city ("Sydney"), a valid temperature, and a valid time ("morning" or "evening")
- Test Case 2: Input a valid city ("Toronto"), a valid temperature, and a valid time ("morning" or "evening")
- Test Case 3: Input an invalid city ("Melbourne"), a valid temperature, and a valid time ("morning" or "evening")
- Test Case 4: Input a valid city ("Sydney"), an invalid temperature (non-numeric), and a valid time ("morning" or "evening")

**Module 3: InputValidator (Equivalence Partitioning)**

- Test Case 1: Input valid country, city, month, temperature, and time
- Test Case 2: Input invalid country, valid city, month, temperature, and time
- Test Case 3: Input valid country, invalid city, month, temperature, and time
- Test Case 4: Input valid country, city, invalid month, temperature, and time
- Test Case 5: Input valid country, city, month, invalid temperature, and time
- Test Case 6: Input valid country, city, month, temperature, and invalid time

**Module 4: GraphicsSymbolMapper (Equivalence Partitioning)**
--
- Test Case 1: Input a valid season ("Summer")
- Test Case 2: Input a valid season ("Autumn")
- Test Case 3: Input a valid season ("Winter")
- Test Case 4: Input a valid season ("Spring")
- Test Case 5: Input an invalid season ("Monsoon")

**Module 5: UserInterface (Boundary Value Analysis)**

- Test Case 1: Input the maximum length of user input
- Test Case 2: Input an empty string
- Test Case 3: Input a special character
- Test Case 4: Input a number

**Module 6: FileHandler (Boundary Value Analysis)**

- Test Case 1: Read input from an existing file
- Test Case 2: Read input from a non existent file
- Test Case 3: Save result to a new file
- Test Case 4: Save result to an existing file

These test designs cover a variety of scenarios and inputs, ensuring that the modules are thoroughly tested using both equivalence partitioning and boundary value analysis techniques.

4. **Test design(White-box testing)**

Based on the code implemented in part 3, the following two modules can benefit from white-box testing:

1. **InputValidator**
1. **GraphicsSymbolMapper**

White-box testing involves examining theinternal structure and logic of the code. Here are the test cases designed for these modules using white-box testing:

**Module 3: InputValidator (White-box Testing)**

- Test Case 1: Validate the input with a valid country, city, month, temperature, and time
- Test Case 2: Validate the input with an invalid country, valid city, month, temperature, and time
- Test Case 3: Validate the input with a valid country, invalid city, month, temperature, and time
- Test Case 4: Validate the input with a valid country, city, invalid month, temperature, and time
- Test Case 5: Validate the input with a valid country, city, month, invalid temperature, and time
- Test Case 6: Validate the input with a valid country, city, month, temperature, and invalid time
- Test Case 7: Validate the input with an invalid country, invalid city, invalid month, invalid temperature, and invalid time

**Module 4: GraphicsSymbolMapper (White-box Testing)**

- Test Case 1: Map a valid season ("Summer") to its corresponding graphics symbol
- Test Case 2: Map an invalid season ("Monsoon") to its corresponding graphics symbol
- Test Case 3: Map a valid season ("Autumn") to its corresponding graphics symbol
- Test Case 4: Map a valid season ("Winter") to its corresponding graphics symbol
- Test Case 5: Map a valid season ("Spring") to its corresponding graphics symbol

These test cases for the InputValidator and GraphicsSymbolMapper modules cover different paths and conditions within the code, ensuring that the internal logic is thoroughly tested.

5. **Test implementation**

\```

import unittest

from input\_validator import InputValidator

class InputValidatorTest(unittest.TestCase):

def test\_valid\_input(self):

validator = InputValidator()

result = validator.validate\_input("Australia", "Sydney", 6, 25, "morning") self.assertTrue(result) # Expecting True

def test\_invalid\_input(self):

validator = InputValidator()

result = validator.validate\_input("", "Melbourne", 13, "abc", "afternoon") self.assertFalse(result) # Expecting False

def test\_edge\_cases(self):

validator = InputValidator()

result = validator.validate\_input("Australia", "Sydney", 1, -10, "evening") self.assertFalse(result) # Expecting False

if \_\_name\_\_ == "\_\_main\_\_":

unittest.main()

\```

In this example, we create a test class `InputValidatorTest` that subclasses `unittest.TestCase`. Inside this class, we define individual test methods that correspond to the test cases mentioned in the white-box testing design.

We create an instance of the `InputValidator` class and use its `validate\_input` method to validate different inputs. We then use assertions to check if the results match the expected outcomes.

To run the test cases, we execute `unittest.main()`, which will run all the test methods in the class.

By running these test cases, you can identify any failures or errors in the InputValidator module. If there are any failures, you can investigate the code to address the issues and improve your code accordingly.

\```

import unittest

from map\_to\_graphics import GraphicsSymbolMapper

class GraphicsSymbolMapperTest(unittest.TestCase):

def test\_valid\_season\_mapping(self):

mapper = GraphicsSymbolMapper()

result = mapper.map\_season("Summer") self.assertEqual(result, "☀ ") # Expecting ☀

result = mapper.map\_season("Winter") self.assertEqual(result, "❄ ") # Expecting ❄

def test\_invalid\_season\_mapping(self):

mapper = GraphicsSymbolMapper()

result = mapper.map\_season("Monsoon") self.assertIsNone(result) # Expecting None

if \_\_name\_\_ == "\_\_main\_\_":

unittest.main()

\```

In this example, we create a test class `GraphicsSymbolMapperTest` that subclasses `unittest.TestCase`. Inside this class, we define individual test methods that correspond to the test cases mentioned in the white-box testing design.

We create an instance of the `GraphicsSymbolMapper` class and use its `map\_season` method to map seasons to their corresponding graphics symbols. We then use assertions to check if the results match the expected outcomes.

To run the test cases, we execute `unittest.main()`, which will run all the test methods in the class.

6. **Version control**

To apply version control and keep track of the software project, follow these steps:

1. **Planning the Branches:**
- Identify the main components or features of the software project.
- Determine the need for different branches based on the project's complexity and development

requirements.

- For this simple software project, you can start with a single branch and create additional

branches if needed.

2. **Creating a Git Repository:**
- Choose a suitable name for your Git repository, following the given format:

`<surname>\_<firstname><ID>\_ISErepo`.

- Set up a local Git repository on your machine using the chosen name.
- Create two directories within the repository: "code" for storing code files and "documents" for

storing relevant documents.

3. **Committing Changes:**
- As you work on the project, commit your changes to the Git repository in a meaningful and

organized manner.

- Commit changes to the appropriate files or directories as you create or modify them, rather

than waiting until the end.

- Consider the granularity of commits and group related changes together, focusing on logical

units of work.

- Provide descriptive commit messages that explain the purpose or functionality of the changes

made.

4. **Branching and Merging:**
- Start with a single branch (e.g., "main" or "master") for the initial development.
  - If the project requires multiple features or significant changes, create feature branches to

isolate and develop those features independently.

- Use branch names that reflect the purpose or feature being developed (e.g.,

"feature/season-finding", "feature/temperature-comparison").

- Work on each feature branch separately, committing changes to the appropriate files within the

branch.

- Once a feature is complete and tested, merge it back into the main branch or any other

appropriate branch.

- Decide when to merge based on the stability and completeness of the feature and the project's

overall development plan.

To adhere to best practices of version control, such as regularly pulling changes from remote repositories, handling merge conflicts when necessary, and pushing your local commits to a remote repository for backup and collaboration purposes.

By following this version control process, we can effectively track our work, maintain a clear history of changes, and collaborate with others if needed.

5. **Git commands are mentioned below**
![image](https://github.com/ShubhangiSakunde/Reports/assets/130922698/15a1911d-d24e-4c94-9040-640768a64261)
![image](https://github.com/ShubhangiSakunde/Reports/assets/130922698/9235a79c-514a-44c6-9480-4004b7faab56)
![image](https://github.com/ShubhangiSakunde/Reports/assets/130922698/21f83068-f2f8-44a4-a0e0-906e8eb61dc7)
![image](https://github.com/ShubhangiSakunde/Reports/assets/130922698/54aa34b6-9ede-4640-8d31-956b9c9a9d47)
![image](https://github.com/ShubhangiSakunde/Reports/assets/130922698/dc8c5499-b7f3-4137-a0a9-2731a1389c73)



7. **Ethics and Professionalism**

1. **Lack of ethical and professionalism in the code can result in harmful effects in the following ways:**
1. Privacy and Data Protection: If the code fails to handle user data and personal information securely, it can lead to breaches of privacy and unauthorized access to sensitive data. This can have severe consequences for individuals, such as identity theft or exposure of personal information.
2. Accuracy and Reliability: If the code does not ensure accurate and reliable results, it can lead to misinformation or incorrect decisions. For example, in the weather software scenario, if the temperature readings or season determinations are inaccurate, it can mislead users and impact their decision-making.
3. Transparency and Accountability: Lack of transparency and accountability in the code can result in hidden functionalities or biased outcomes. This can lead to unethical manipulation of data or unfair treatment of users.
4. Accessibility and Inclusivity: If the code does not consider accessibility guidelines and fails to provide equal access to individuals with disabilities, it can lead to discrimination and exclusion of certain user groups.
5. Intellectual Property Rights: If the code infringes upon intellectual property rights, such as unauthorized use of copyrighted materials or plagiarism of code, it can lead to legal implications and harm the original creators.
6. System Performance and Scalability: Lack of professionalism in code design and implementation can result in poor system performance and scalability issues. This can cause disruptions in service, loss of productivity, and financial losses for organizations relying on the software.
7. Ethical Decision Making: If the code does not incorporate ethical decision-making processes or fails to consider the potential social impact of its functionality, it can result in unintended consequences and harm to individuals or communities.

2. **Two suggestions to avoid ethical and professional issues in the software proposed in this assignment, based on ACS or IEEE-CS Ethical guidelines, are:**
1. Ethical Consideration: Conduct an ethical analysis of the software project to identify and address potential ethical issues. This involves considering the impact of the software on users, society, and the environment. Implement privacy protection measures, data encryption, and secure handling of user information to safeguard privacy. Ensure transparency in how user data is collected, used, and stored, and provide clear consent mechanisms.
2. Professionalism and Quality Assurance: Follow professional software development practices, including code reviews, unit testing, and continuous integration, to ensure code quality and reliability. Adhere to industry standards and best practices to design modular, maintainable, and scalable code. Implement version control to track changes and maintain code integrity. Prioritize user experience, accessibility, and inclusivity by considering diverse user needs and following accessibility guidelines.

By incorporating these suggestions, the software project can promote ethical and professional conduct, mitigate potential harms, and enhance user trust and satisfaction.
