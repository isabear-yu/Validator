
# XML Validator
Given a String of `xml`, return `true` if it's a valid XML string, and `false` otherwise.

XML naming rules:
* Must have opening tag and closing tag.
* Case-sensitive.
* Must be properly nested and in correct orders.
* Permissible for the element name to include other character such as "<," "&,", "/", ":" or " ".
* Permissible for the element name to include spaces
* No extra contents outside of the XML tag

## There are three files in the folder
- `App.java` : Run the main method in `App.java` to see the printed output.
- `SimpleXmlValidator.java` : The function to determine whether or not a string is a valid XML string.
- `TestXmlValidator.java` : Mutilple Junit test cases

## Test the function with JUnit testing framework

### Requirements
- JDK (version 1.8 or later)

- Visual Studio Code (version 1.59.0 or later)

- Extension Pack for Java: Navigate to `Extensions` tab on the left -> type `Extension Pack for Java` and install -> Navigate to `Testing` tab on the left and click `Enable Java Test` -> Choose `JUnit`

## JUnit testing case

**TestMustHaveOpeningAndClosingTag**:

Input: `<Design><Code>hello world</Code></Design>`

Output: `true`

Input: `“null” `

Output: `false`

Input: `“”`

Output: `false`

Input: `“ ”`

Output: `false`

Input: `<Design><Code>hello world`

Output: `false`

Input: `hello world</Code></Design>`

Output: `false`

Input: `hello world`

Output: `false`


**TestCaseSensitiveTag**

Input: `<Design><Code>hello world</Code></Design>`

Output: `True`

Input: `<design><code>hello world</Code></Design>`

Output: `false`


**TestProperlyNestedAndCorrectedOrder**

Input: `<Design><Code>hello world</Code></Design>`

Output: `True`

Input: `<Design><Code>hello world</Code</Design>`

Output: `true`

Input: `<People><Code>hello world</People></Code>`

Output: `false`

Input: `<Design><Code>hello world</Code></Design`

Output: `false`



**TestElementsCanHaveAnyCharacter**

Input: `<Design$:><Code/Peolpe>hello world</Code/Peolpe></Design$:>`

Output: `true`

Input: `<Design><Code>>&>hello world</Code<%<</Design>`

Output: `true`

Input: `<<></<>`

Output: `true`

Input: `<:></:>`

Output: `true`

**TestElementsCanHaveSpace**

Input: `<Design >< Code>hello world</ Code></Design >`

Output: `true`

Input: `< ></ >`

Output: `true`

**TestNoContentsOutsideOfTags**

Input: `hello world<Code>Hello World</Code>hey`

Output: `false`



















