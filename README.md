🎂 Interactive Recipe Cost Calculator
This Python script is a simple, interactive tool that helps you calculate the total cost of a recipe based on the individual prices and quantities of its ingredients. It's especially useful for small businesses or home bakers who want to accurately price their products.

✨ Features
User-Friendly Interface: The program guides you through adding each ingredient one by one.

Cost Calculation: It automatically calculates the cost of the specific amount of an ingredient you use in your recipe, even if you bought a larger package.

Input Validation: It ensures that only valid numeric input is accepted, preventing common errors.

Final Summary: After you've added all your ingredients, it provides a clear breakdown of each item's cost and the final total cost of the recipe.

🚀 How to Use
Clone the Repository: First, you need to get the code. Open your terminal or command prompt and run the following command:

Bash

git clone [repository-url]
Run the Script: Navigate to the project directory and execute the script using a Python interpreter:

Bash

python recipe_calculator.py
Follow the Prompts: The program will prompt you for the following information for each ingredient:

Ingredient Name: The name of the ingredient (e.g., "farinha de trigo", "ovos").

Recipe Quantity: The amount you are using in the recipe (e.g., 200).

Unit: The unit of measurement (e.g., g, ml, un).

Package Size: The size of the package you bought from the store (e.g., 1000 for a 1 kg bag, 12 for a dozen eggs).

Package Price: The price of that specific package (e.g., 2.50).

Finish: Once you have entered all your ingredients, simply press Enter on an empty prompt to see the final cost breakdown.

💻 Code Explanation
The script is structured with two main functions:

get_numeric_input(prompt): This is a helper function that handles user input. It's designed to continuously ask the user for a number until a valid, non-negative value is entered. It also handles common user mistakes, such as using a comma (,) instead of a period (.) for decimals.

calculate_interactive_recipe_cost(): This is the main function that orchestrates the entire process. It initializes a list to store ingredients and a variable for the total cost. It then enters a while loop that continues to prompt the user for ingredient details until they choose to finish. Inside the loop, it calls the get_numeric_input helper function to collect data and then calculates the cost of the ingredient using this formula:

Cost per ingredient= 
Package size
Quantity used
​
 ×Package price
$$$$Finally, it prints a clean and formatted summary of all ingredients and the total recipe cost.
