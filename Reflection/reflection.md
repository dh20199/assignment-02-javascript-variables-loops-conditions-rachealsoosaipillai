# Reflection

## Question 1 (50 words)
#### When and why should you use a function like `carefulSubract` rather than `subtract`? 
> A function like carefulSubtract should be used whenever the input types are not guaranteed to be numbers. Since carefulSubstract checks that both inputs are valid numbers before subtracting them, it is usually better to use carefulSubtract in most cases. Also, carefulSubtract gives the user a helpful message in the case of invalid inputs whereas subtract may return an unexpected result or a less helpful error message.

## Question 2 (100 words)
#### What are `data types`, and how does data typing work in JavaScript? Name at least 4 built-in data JS data types. 
> A data type is an attribute of data that instructs a compiler or interpreter on how a programmer expects the data to be used. Many programming languages support commonly used data types such as real numbers, integers, and booleans.
>
> JavaScript is a dynamic language. This means that variables in JavaScript are not directly associated with a specific type of value. Any variable can be assigned, and re-assigned, a value of any type.
>
> Some built-in data types in JavaScript are Boolean (i.e. two truth values in logic, true or false), Number, String, and Object. The Object data type is not primitive because it refers to a data structure that consists of data and instructions for working with the data.

## Question 3 (100 words)
#### What is the advantage to storing information as an object (`{firstName: 'Italo', lastName: 'Calvino', profession: 'novelist' }`) rather than as an array (`['Italo', 'Calvino', 'novelist']`)? Are there any disadvantages?
> The advantages to storing information as an object are clarity and structure. By looking at the string representation of this object, it is clear what the purpose of each property is and what kind of value that property will contain. In this case, we can tell that firstName, lastName, and profession are common properties for this object and they're of type String. This object also provides structure and readability since we can get the value of a property we're interested in using syntax such as `object.profession` and it's clear to readers what this value could be in comparison to something like `array[2]`.
>
> However, if the order of elements is important then it's better to use an array so that order is guaranteed. Objects do not guarantee order like arrays, but they provide quick lookup for key-value pairs (e.g. `object.profession` is a key for value novelist).

## Question 4 (150 words)
#### The function `sentences` transforms a data structure (in this case, a list of object literals) into a sequence of sentences. If the data structure were less predictable (e.g., if some properties of each object were occasionally missing, or if their data type was not always the same), what programming techniques could you use to ensure that your function produced a coherent output? Also, can you think of a more interesting "transform" that could be done with the same data structure?
> When a data structure is less predictable, the programmer will have to add conditions to check the number of inputs and their types before attempting to do an operation with the inputs in order to avoid returning incorrect results or errors. For example, the programmer should verify that if an object has the `from` and `to` properties, that these properties hold `Number` values that are years so that subtraction would have a meaningful result. This can be achieved by creating helper functions like `isValidYear` to check that a value like `2015` has a `typeof` 'number' and is within some expected date range like `1867-2019`.
>
> Another transform that could be done with the same data structure passed into `sentences` is to determine the number of prime ministers per political party. For example, if given a list of prime ministers each with their `party` property holding a valid value, we can compute how many of these prime ministers belonged to the Conservative, Liberal, and other parties. Then we can display this information in a bar graph where each `party` is a category its numerical value represents how many prime ministers belonged to that political party.