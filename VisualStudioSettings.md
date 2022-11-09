# Onboarding - Visual Studio Settings
We have some common visual studio setting we want all developers to configure for their visual studio installation(s). 
These will help make your life as a developer easier as well as ensure your Visual Studio if formatting code files correctly to be consistant with Contexture's coding standards and the rest of the team so no one has to spend their time reviewing whitespace changes or formatting code.






# Overview
1. [C# Keybindings](https://github.com/AdamAtCorhio/Documentation/new/main#keybindings)
2. [Visual Studio Project Templates](https://github.com/AdamAtCorhio/Documentation/new/main#visual-studio-project-templates)
3. [.editorconfig](https://github.com/AdamAtCorhio/Documentation/new/main#editorconfig)
4. [Naming Styles](https://github.com/AdamAtCorhio/Documentation/new/main#naming-styles)
5. [General guidelines & Suggestions](https://github.com/AdamAtCorhio/Documentation/new/main#general-guidelines--suggestions)




---






## Keybindings

In Visual Studio, go to Tool -> Options
In the options dialog, select Keyboard and make sure the dropdown at the top of the right panel has 'Visual C# 2005' selected:


![Obey Projects' .editorconfig Settings](https://github.com/AdamAtCorhio/Documentation/blob/main/images/csharp-keybindings.png)

This allows you to use Visual Studio C# shortcuts when coding, such as F2 to rename the object at the caret cursor, and all instances in scope, or F12 to go the definition of the object at the caret cursor.





---







## Visual Studio Project Templates

We have a Visual Studio Project Template you can install, which will add a Connexion Device Project type available in Visual Studio when creating a new project.

First download the [Contexture_ConnexionDeviceLibrary.zip]([https://github.com/AdamAtCorhio/ConnexionDeviceProjectTemplate/raw/main/CORHIO_ConnexionDeviceLibrary.zip](https://github.com/AdamAtCorhio/ConnexionDeviceProjectTemplate/raw/main/Contexture_ConnexionDeviceLibrary.zip)) archive and
 extract/place the Contexture Connexion Device Library folder into the following location:
 
 
`C:\Users\[YOUR_USERNAME_HERE]\Documents\Visual Studio 2022\Templates\ProjectTemplates\Visual C#\`

(Note: You may need to turn that 2022 into a 2019 if you have an older version of Visual Studio installed.)

How to use: When creating a new project in Visual Studio, just search for Connexion or Contexture and select the Connexion Device project type.





---







## .editorconfig

In Visual Studio, go to Tool -> Options
In the options dialog, select Text Editor -> General and ensure the 'Follow project coding conventions' checkbox is checked:


![Obey Projects' .editorconfig Settings](https://github.com/AdamAtCorhio/Documentation/blob/main/images/obey-project-editorconfig.png)

This will ensure your visual studio conforms to the formatting specified in the project.






---






## Naming Styles

In Visual Studio, go to Tool -> Options
In the options dialog, select Text Editor -> C# -> Code Style -> Naming

We are going to add 3 sections.
 
![Screenshot](https://github.com/AdamAtCorhio/Documentation/blob/main/images/Picture1.png)

#### Private or Internal Field 

1. Click Manage Specifications 

![Screenshot](https://github.com/AdamAtCorhio/Documentation/blob/main/images/Picture2.png)

2. Ensure Private or Internal Field looks as above 

3. Click Manage Styles 

4. Click New 

![Screenshot](https://github.com/AdamAtCorhio/Documentation/blob/main/images/Picture3.png)

5. Enter these fields for Private _ 

![Screenshot](https://github.com/AdamAtCorhio/Documentation/blob/main/images/Picture4.png)

6. Click add new Rule 

![Screenshot](https://github.com/AdamAtCorhio/Documentation/blob/main/images/Picture5and7.png)

7. Fill in Private or Internal Field and Private _ and SUGGESTION and click the Reorder arrows until it is the first option. 







#### Enum

1. Click Manage Styles and add a new Style 

![Screenshot](https://github.com/AdamAtCorhio/Documentation/blob/main/images/Picture6.png)

2. Click add new Rule 

![Screenshot](https://github.com/AdamAtCorhio/Documentation/blob/main/images/Picture5and7.png).png)

3. Choose Enum and All Upper and Separated by _ and ERROR and move it to second highest slot by the Reorder arrows. 





#### Interface
 * Ensure Interface, Begins With I and ERROR are present in the list. 


#### Types
 * Ensure Types and Pascal Case and ERROR are present in the list. 


#### Non-Field Members
 * Ensure Non-Field Members and Pascal Case and Error are present in the list.  




---





## General guidelines & Suggestions

#### You are unique. Your code should not be.

If you notice the code establishes a pattern by doing similar or repetitive tasks by the same approach every time, and you have to add another method that accomplishes a similar task but for a different health care provider, follow the established pattern and take the same approach, use the same naming scheme, etc. 

Similarly, establish patterns. Do the same things the same way every time.

This consistancy allows someone reading to code to consume and comprehend the code much quicker and with less mental effort. 
Imagine 5 different methods that have very similar workflows and that all look similar, from the name of the methods and the ordering of the steps the then temporary variable names. 
Contrast that to the same 5 methods but where each one is a unique and special flower, each accomplishing the task using a different approach, in a different order and calling different helper libraries and different naming convention.
In the former scenario, someone trying to understand the entire code file only has to carfully read and understand one method. Then, by visually identifying other methods that have the same shape and look, they can ignore them, scrolling past and continuing their search for the particular method or bug or whatever they are seeking, know that those other methods are essentially doing the same thing.

Example:
If I am writing a method that constructs or populates a class or some result with the intent of returning that class or result from that method, I always give the variable that will eventually be returned the name: `result`. This makes all such methods easier to understand and an obvious place to look if someone is trying to understand what types of values it might return or track down a bug with the value its returning.






