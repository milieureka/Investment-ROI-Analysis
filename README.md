# Investment Calculator

## Language:
C#, Newtonsoft.Json, .NET Application.

## Overview
The Investment Calculator is a risk assessment tool designed to calculate and assess soley or porfolio investment. This application fetch real data from internet and leverages object-oriented principles to manage user choice of investment (stock/ bond), investment portfolios risk assessments.

**ROI** is calculated as:

$ROI = \left( \frac{\text{Current Value of Investment} - \text{Cost of Investment}}{\text{Cost of Investment}} \right) \times 100\%$

**P\&L** is determined by:

$\text{PnL} = \text{Current Value of Investment} - \text{Cost of Investment}$

**Risk assessment** specifically through the standard deviation of returns

$\text{Risk (Standard Deviation)} = \sqrt{\frac{1}{N-1} \sum_{i=1}^{N} (R_i - \bar{R})^2}$

Where:
- $`R_i`$ is the return of the investment in the ith period,
- $`\bar{R}`$ is the average return of the investment,
- $`N`$ is the total number of observations.

**UML Diagram** 
![UML Diagram](https://github.com/milieureka/Investment-Calculator/blob/main/UML%20Class%20diagram-Investment%20Program-1.png)

## Object-Oriented Programming (OOP) Concepts Details
- Inheritance: BondInvestment and StockInvestment inherit from the abstract class Investment, which defines shared properties and methods like amountInvested, roi, and AssessRisk.
- Encapsulation: Properties and methods are encapsulated within classes, such as Investment and User, ensuring that data is hidden from external access and is accessible only through methods in the class.
- Polymorphism: Methods like AssessRisk are overridden in derived classes (BondInvestment and StockInvestment), allowing them to implement specific risk assessment logic.

**Class structure**
- UIManagement: Manages user interactions and controls the flow of the application, facilitating operations like creating users, adding investments, and displaying analyses. The public userSelection() method make program responds to user inputs, which guide the program flow.
- User + Portfolio: Handles user data and their investment portfolios. Each User has a Portfolio, which aggregates multiple Investments.
- Risk Assessment: Contains logic to assess the risk of different types of investments. The method AssessBondRisk suggests specialized risk assessment for bonds.
- Investment: use Newtonsoft.Json to retrieving data from online databases (such as Yahoo Finance). Newtonsoft.Json can convert C# objects into JSON and JSON into C# objects (serialization and deserialization, respectively), it is helpful to fetch real-time financial data, which is essential for evaluating the ROI and performance of investments.
- Portfolio: has methods to calculate total ROI and to assess the risk of the entire portfolio, crucial for giving users a holistic view of their investments' performance.
Program Flow 
- The Main() function in the Program class likely initializes the application, setting up necessary components and possibly loading initial data.

## Result
- Enter user information and fetching real-time stock prices.
![fetch stock price](https://github.com/milieureka/Investment-Calculator/blob/main/UML%20Class%20diagram-Investment%20Program-2.png)

- Here, all stock data are presented in a structured JSON format.
![result in JSON format](https://github.com/milieureka/Investment-Calculator/blob/main/UML%20Class%20diagram-Investment%20Program-3.png)

- Risk assessment base on amount Invested and analized ROI & PnL.
![analysis](https://github.com/milieureka/Investment-Calculator/blob/main/UML%20Class%20diagram-Investment%20Program-4.png)

- Showcase portfolio items, type of risks, etc.
![portfolio result](https://github.com/milieureka/Investment-Calculator/blob/main/UML%20Class%20diagram-Investment%20Program-6.png)


## How to Use
1. Clone the repository to your local machine.
2. Ensure you have .NET framework installed.
3. Navigate to the project directory and build the project.
4. Execute the program to start calculating investments.
   
## Contributing
My code aren't perfect, I want to adjust the logic of risk assessment to be more robust. Feel free to fork the repository and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Contact
If you have any questions or feedback, please contact me at discussion.
