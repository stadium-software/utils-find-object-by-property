# Find Object By Property

A script to find an object in a List of objects by a property and value of the object

# Version 

1.0 Initial

# Global Script Setup
1. Create a Global Script called "FindObjectByProperty"
2. Add the input parameters below to the Global Script
   1. List
   2. Property
   3. Value
3. Add the output parameter below to the Global Script
   1. Result
4. Drag a *JavaScript* action into the script
5. Add the Javascript below into the JavaScript code property
```javascript
/* Stadium Script 1.0 https://github.com/stadium-software/utils-find-object-by-property */
let arr = ~.Parameters.Input.List;
if (!arr) arr = [];
let property = ~.Parameters.Input.Property;
let value = ~.Parameters.Input.Value;
return arr.find(item => item[property] === value);
```
6. Drag a *SetValue* action into the Global Script and place it under the *JavaScript* action
   1. Target: = ~.Parameters.Output.Result
   2. Value: = ~.Javascript

## Usage
1. Drag the script called "FindObjectByProperty" into a script or event handler
2. Enter values for the script input parameters
   1. List: A List of objects
   2. Property: The name of the property to locate
   3. Value: The value the property to locate
3. Result: The script returns the first object that matches