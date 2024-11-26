# Node.js Beginners Week 2

## Main Topics

* Functions
    - [Net Ninja](https://www.youtube.com/watch?v=xUI5Tsl2JpY)
    - [Elzero Web School](https://www.youtube.com/playlist?list=PLDoPjvoNmBAx3kiplQR_oeDqLDBUDYwVv) [57:70]
* Higher Order Functions
    - [Traversy Media](https://www.youtube.com/watch?v=rRgD1yVwIvE)
    - [Elzero Web School](https://www.youtube.com/playlist?list=PLDoPjvoNmBAx3kiplQR_oeDqLDBUDYwVv) [71:78]
* Objects
    - [Net Ninja](https://www.youtube.com/watch?v=X0ipw1k7ygU)
    - [Elzero Web School](https://www.youtube.com/playlist?list=PLDoPjvoNmBAx3kiplQR_oeDqLDBUDYwVv) [79:85]
* Hoisting
    - [Colt Steele](https://www.youtube.com/watch?v=j-9_15QBW2s)
    - [Shadow Coding](https://www.youtube.com/watch?v=XrCMAmxGA7o)

## Extra Resources

* Array Methods & Higher Order Functions
    - [Florin Pop](https://www.youtube.com/playlist?list=PLgBH1CvjOA62PBFIDq55-S6Beivje30A2)
* Usage of logical OR
    - [Unique Coderz Academy](https://www.youtube.com/watch?v=u7eGlZMimDU)


## Task


### Theoritical
* Explain the difference between primitive types and reference types in JavaScript.
* Compare the two methods of creating a new function in JavaScript: Function Declaration and Function Expression. Discuss the differences between them in terms of hoisting and provide examples for each.
* Research the concept of "Pure Function" and then respond to the following: Under what conditions can a function be classified as a pure function?
* Write down the array methods that you have studied and classify them to **destructive** and **not destructive**.
* Answer few MCQ questions in the submission form.

### Practical

#### Inventory Management System

Create a basic inventory management system in JavaScript.

##### Instructions:

* Create Item Objects

    - Define an createItem function that takes name, category, price, and stock as parameters and returns an item object.
    - Include methods within the item object to:
        * `updateStock(newStock)`: Updates the stock level of the item.
        * `applyDiscount(discount)`: Applies a discount to the item's price.

* Create an Inventory Object

    - Define an inventory object that initializes an empty array to store items.
    - Add methods to the inventory object to:
        * `addItem(item)`: Adds an item to the inventory.
        * `removeItem(itemName)`: Removes an item from the inventory by its name.
        * `getItem(itemName)`: Retrieves an item from the inventory by its name.
        * `filterItems(predicate)`: Uses a higher-order function to filter items based on a given predicate function.

* Create several item instances and add them to the inventory.

    - Update stock and apply discounts to certain items.
    - Use the `filterItems` method to find items under a specific category or below a certain stock level.
    - Remove an item from the inventory and verify it is no longer available.
    - Ensure proper handling of cases where item details might be missing or undefined, using logical OR.