The Community of Christ Directory Generator is a macro-enabled Excel spreadsheet which converts a spreadsheet tab labeled "Directory" into a formatted Word document. 

This tool requires the "Microsoft Office XX.X Object Library" reference to be enabled. 
The reference can be added from the Tools > References dropdown from the Visual Basic interface. 

The "Instructions" sheet contains useful information on how to use the macros. This sheet also contains macro settings, such as information to put on the header page
and options to use when generating the directory file. 

The following fields are available to include on the Header Page:

-Congregation Name
--Congregation Name is a required parameter.
--Congregation Name represents the name of the congregation of which the directory represents.

-Street Address
--Street Address is an optional parameter.
--Street Address represents the street address of the congregation's building. 

-City
--City is a required parameter if Street Address is provided. Else, it is an optional parameter.
--City represents the city of the street address provided. 

-State
--State is a required parameter if Street Address is provided. Else, it is an optional parameter.
--State represents the US state (including D.C.) of the street address provided.

-Zip
--Zip is a required parameter if Street Address if provided. Else, it is an optional parameter.
--Zip represents the zip code of the street address provided. Only zip codes with format ##### are allowed, zip codes of format #####-#### are not supported.

-Email Address
--Email Address is an optional parameter. 
--Email Address represents the email address to contact church leadership or other email address as desired to represent the congregation.
--The email address on the generated directory will automatically include "mailto:" prepended to the email address to generate a useful hyperlink.

The following Options are available for document generation:

-Include Priesthood Office Table
--If checked, adds a Priesthood Office Table to the end of the directory, sorted by name.

-Keep Word Document Open
--If checked, keeps the Word document open after generating the directory. If unchecked, the Word document generated will automatically be closed.

-Generated PDF and Open
--If checked, generates a PDF from the Word document and opens it in the default PDF viewer for the system. 

-Use Wider Side Margins
--If checked, sets side margins to 1". If uncheck, side margins are set to 0.5". 

-Include Extra Row on Priesthood Office Table
--If checked, includes an extra row after including all necessary rows for data in the Priesthood Office Table for each Priesthood Office.

There are two buttons on the "Instructions" sheet which can be used to generate the document. 

The "Sort" button is used to sort the data on the "Directory" sheet by Household Name, Street Address, and Address ID. 
It is recommended to sort the data before generating the directory.

The "Generate Document" button is used to generate the directory using the options enabled at run-time. 
The data on the "Directory" sheet is not automatically sorted before generating the document. 

The "Directory" sheet is the source data from which the directory is generated. The following fields are included:

-Household Name
--Household Name is a required parameter. 
--Household Name represents the name of the family that lives at the provided address. In most cases, the Household Name field will match the Last Name field.

-Last Name
--Last Name is a required parameter.
--Last Name represents the last name of the individual to include in the directory.
--If the Last Name differs from the Household Name, the Last Name will be explicitly displayed on the generated directory. 

-First Name
--First Name is a required parameter.
--First Name represents the first name of the individual to include in the directory.

-Email Address
--Email Address is an optional parameter.
--Email Address represents the email address of the individual to include in the directory. 
--The email address on the generated directory will automatically include "mailto:" prepended to the email address to generate a useful hyperlink.

-Home Phone Number
--Home Phone Number is an optional parameter.
--Home Phone Number represents a phone number associated with the provided address or Household Name. 
--Home Phone Number should be entered as a 10 digit number. Excel will automatically format the number to be in (###) ###-#### format for both the spreadsheet and the document.

-Mobile Phone Number
--Mobile Phone Number is an optional parameter.
--Mobile Phone Number represents the mobile phone number of the individual to include in the directory. 
--Mobile Phone Number should be entered as a 10 digit number. Excel will automatically format the number to be in (###) ###-#### format for both the spreadsheet and the document.

-Address ID
--Address ID is a required parameter. 
--Address ID is used to determine if a new Household should be generated on the directory document. 
--Address ID should equal 1 for the head of the household and 0 for all members of the household. 

-Stress Address
--Street Address is an optional parameter.
--Stress Address represents the street address of the household to include in the directory.
--Any street address that would use a second line should be combined into a single line.

-City
--City is a required parameter if Street Address is provided. Else, it is an optional parameter.
--City represents the city of the street address provided.

-State
--State is a required parameter if Street Address is provided. Else, it is an optional parameter.
--State represents the US state (including D.C.) of the street address provided.

-Zip
--Zip is a required parameter if Street Address if provided. Else, it is an optional parameter.
--Zip represents the zip code of the street address provided. Only zip codes with format ##### are allowed, zip codes of format #####-#### are not supported.

-Birthday
--Birthday is an optional parameter.
--Birthday represents the birthday of the individual to include in the directory. 
--Birthday can be entered in MM/DD/YY, MM/DD/YYYY, or MM/DD format. However, it is recommended to be consistent. 

-Anniversary 
--Anniversary is an optional parameter.
--Anniversary represents the anniversary of the individual to include in the directory. 
--Anniversary can be entered in MM/DD/YY, MM/DD/YYYY, or MM/DD format. However, it is recommended to be consistent. 

-Priesthood Office
--Priesthood Office is an optional parameter.
--Priesthood Office is only used if the "Include Priesthood Office Table" Option is checked.

When the directory is generated, the data from the "Directory" sheet will be formatted as follows for each household:

Household Name    Home Phone Number    Street Address, City State Zip
    Last Name, First Name    Mobile Phone Number    Email Address    Birthday     Anniversary

Last Name is only displayed if the value is different from the Household Name. 
Information ommitted is not included. 

The "References" sheet is used for data validation and generation of the Header Page. 
It is recommended not to change the content of this sheet. 
However, it is possible to change the image used for the Header Page.
To change the image used on the Header Page:
-Delete the original image.
-Insert the new image onto the same sheet. 
-Change the name of the image to "Header_Image" and press enter.