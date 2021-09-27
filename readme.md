#Service to Convert Integers to Roman Numerals

## Converting Integers into Roman Numerals
Rules for Roman Numeral conversion followed from the following link. 
- [rules](https://www.math-only-math.com/rules-for-formation-of-roman-numerals.html)

### Rules Outlined
- Input must be within bounds (1-3999) explicitly.
- Output for failures are formatted like the following. Contains a success boolean, message and null data.
```
{
    "success": false,
    "message": "Input must be between 1-3999",
    "data": null
}
```
- Output for successful conversions are formatted like the following.  Contains a success boolean, null message and object containing the input and output values.

```
{
    "success": true,
    "message": null,
    "data": {
        "input": 1,
        "output": "I"
    }
}
```

##DTO
- [dto](src/main/java/com/example/romannumeral/dto/)
1. Response formatting that contains success, message and data
1. Return object in response.

##ENUMS
- [enums](src/main/java/com/example/romannumeral/enums/)
1. Error Responses returned to user.
1. List of numbers and their base roman numeral letter.  A map is compiled off this enum.

##REST
- [rest](src/main/java/com/example/romannumeral/rest/)
1. API endpoints.  No validation currently.

##service
- [service](src/main/java/com/example/romannumeral/service/)
1. Brains of the project where all the business logic is completed to turn a number into a roman numeral.

##Validation 
- [ValidateRomanNumeralInput](src/main/java/com/example/romannumeral/validation/ValidateRomanNumeralInput.java)
1. Validated input isn't null.
1. Validated input is within bounds.

##Tests 
- [tests](src/test/java/com/example/romannumeral/)
1. Tested the service and validation class.

##Running App
1. Run the application locally through your favorite IDE.  
1. Open postman
1. Change the query param to whatever value you want to convert. 
```
http://localhost:8080/romannumeral/query=1
```
