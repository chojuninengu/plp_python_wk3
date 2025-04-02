# Discount Calculator

This repository contains a Python function named `calculate_discount` that calculates the final price of an item after applying a discount. The function takes the original price and the discount percentage as parameters. If the discount percentage is 20% or higher, it applies the discount; otherwise, it returns the original price.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Example](#example)
- [Contributing](#contributing)
- [License](#license)

## Installation

To use the `calculate_discount` function, you need to have Python installed on your machine. You can download Python from the [official website](https://www.python.org/).

## Usage

1. **Import the Function**:
   - Copy the `calculate_discount` function into your Python script or import it from a module if you save it in a separate file.

2. **Call the Function**:
   - Pass the original price and the discount percentage as arguments to the `calculate_discount` function.
   - The function will return the final price after applying the discount if the discount percentage is 20% or higher. Otherwise, it will return the original price.

## Example

Here is an example of how to use the `calculate_discount` function in a script that prompts the user for input:

```python
def calculate_discount(price, discount_percent):
    """
    Calculate the final price after applying a discount.

    Parameters:
    price (float): The original price of the item.
    discount_percent (float): The discount percentage to apply.

    Returns:
    float: The final price after applying the discount, or the original price if the discount is less than 20%.
    """
    if discount_percent >= 20:
        discount_amount = price * (discount_percent / 100)
        final_price = price - discount_amount
        return final_price
    else:
        return price

# Prompt the user to enter the original price and the discount percentage
original_price = float(input("Enter the original price of the item: "))
discount_percentage = float(input("Enter the discount percentage: "))

# Calculate the final price using the calculate_discount function
final_price = calculate_discount(original_price, discount_percentage)

# Print the final price
print(f"The final price after applying the discount is: {final_price}")
