
## Namespace and Class

- Both are named OnspringImportFileGenerator
- Class is labeled as:
  
  ```csharp
public OnspringImportFileGenerator : Form
```

	- : Form inherits from `System.Windows.Forms.Form` which is provided by the .NET Framework's Windows Forms library. The `Form` class is located in the `System.Windows.Forms` namespace, which contains all the classes needed to build Windows desktop applications with graphical user interfaces.
	- This is used to build the Onspring OFIG GUI. 
- After the declaration of namespace and class, there a long list of variables starting on line 46 and ending on  380.

## Global Variables

- Lines 54 - 59 are declared as: 
  ```  csharp
	readonly string exampleString = Application.StartupPath
```

	`Application.StartupPath` is a property in the `System.Windows.Forms` namespace that returns the directory path where the executable file that started the application is located, _excluding_ the executable file name itself. Please see this reference [Application.StartupPath Property](https://learn.microsoft.com/en-us/dotnet/api/system.windows.forms.application.startuppath?view=windowsdesktop-9.0)
	
- After these, lines 59-115 declare a long group of strings, each string is declared with the associated value of `string.Empty`.
	- These string a placeholders and will later be assigned values. 
	- These are set up to pass the following:
		  - file and file paths for Prodline, Devices, Device updates, Users, User updates, User emails, Managers, Markets, Ministries, Porfolio Teams, Apps, Instances, Device lists, Device lists updates.
	- Lines 95-111 establish empty strings for RSOgroupName, RSOMGRgroupName, LSOgroupName, RSOLSOgroupName, and DEFgroupName. There are 3 different sets of strings that get established for this for the 3 different environments (Dev, Test, and Prod).
	- Lines 113-116 sets up an empty string to later be populated with the inbound and outbound server name and server path. 
	- Lines 118-120 seems to establish archival variables and rules. 
	- 121-128 is a series of bool variables. Looks like it will be used to check a series of conditions based on devices.
	- Lines 130-155 declare a series of lists. Some info on some of the lists:
		- uniqueDeviceTypes and uniqueDeviceOS are global lists to pass of these values.
		- 145-152 Checks for a number of items to skip and store the skipped values in several lists.
		- 153-155 stores the remaining unskipped values into three lists RSOfound, LSOfound, RSOMGRfound. 
	- Lines start to declare variables that will assist in building and formatting the new reports that will be sent to the DMZ server for Onspring to pick up. 
		- 164 and 165 sets the start time and start date using the dotnet system library of `DateTime`.
		- 171-190 establishes the columns numbers and names for the device list.
		- 194-339 establishes the columns numbers and names for the product line.
		- 343-356 establishes the columns numbers and names for the users updates.
		- 360-364 establishes the columns numbers and names for the users email.
		- 366-380 esteblishes a number of strings realted to names, usernames, emails, IDs, and groups.

## Onspring Import File Generator Load

A method `OnspringFileImportFileGenerator_Load` is declared as a void return.

- It checks if 5 different files exist and if they do, then it uses `BuildString` and `AdjustLog` to build and update log files.  
-   The `BuildString()` is used some third-party libraries (**Ex.** FlexGrid) to serialize style definitions as a string. **Ex.** `CellStyle.BuildString()`
- Then, an array is declared `string[] args = System.Evironment.GetCommandLineArgs` 
	- This retrieves all the command-line arguments passed to the currently running process and stores them in a string array called `args`.
	- It runs  a loop through the args array and checks for a series of conditions. 
	- It looks for a set of characters "/?", which it identifies as a help switch. It then class a class "Form2" which contains a number of methods. RootPath, StartupTopic, ShowDialog are called from the Form2 class. 