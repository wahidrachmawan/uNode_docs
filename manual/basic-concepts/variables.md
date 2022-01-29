# Variables

A typical program uses various values that may change during its execution. For example, a Enemy script that has a health value. The health value used by one Enemy may differ from another Enemy like a Boss and a Warrior that's use single script. Hence this makes it necessary to use variables as another Enemy script may not use the same values. So basically, a Variable is a placeholder of the information which can be changed at runtime. And variables allows to `Retrieve` and `Manipulate` the stored information.

Characteristics of Variables:

- **name**  : It must be a valid identifier.
- **type**  : It defines the types of information which is to be stored into the variable.
- **value** : It is the actual data which is to be stored in the variable

Rules for Naming Variables

- Variable names can contain the letters ‘a-z’ or ’A-Z’ or digits 0-9 as well as the character ‘_’.
- The name of the variables cannot be started with a digit.
- The name of the variable cannot be any [C# keyword](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/) say int, float, null, string, etc.

