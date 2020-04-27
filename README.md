# Qlik Sense Courses Tracker Dashboard
A Qlik Sense dashboard to track course progress at Qlik Continuous Classroom (QCC).
  
## Table of contents  
| File name                    | Description                        | 
| ---------------------------- | ---------------------------------- |
| [QCC] Course Dashboard.qvf   | Qlik Sense dashboard file          |  
| QCC.xlsx                     | Excel database file                |
| SimpleFieldSelect-master.zip | Qlik Sense extension zipped folder |
  
About the Excel database file:
The database has the same topic structure from former QCC Business Analyst and Data Architect courses.  
 
## How to use 
### Database file
#### First tab: QSBA
Your progress must be filled in the column **Completed** at QSBA tab in the QCC.xlsx database, with the number of minutes you have already completed in the course. 
*E.g.:*  
  
Tab: **QSBA**
| Role             | Stage | Part # | Part            | Chapter	                                     | Minutes | Completed |
| ---------------- | ----- | ------ | --------------- | -------------------------------------------- | ------- | --------- |
| Business Analyst | Basic |      1 | Getting Started | Orientation to the Qlik Continuous Classroom |      17 |        17 |
| Business Analyst | Basic |      1 | Getting Started | Getting Started with Qlik Sense	             |      67 |         0 |
| Business Analyst | Basic |      1 | Getting Started | Why Analytics                                |      11 |         0 |

#### Second tab: QSDA
In the second tab, the green-colored columns must **not** be changed due to their formulas. Your progress must be filled **only** in the **Completed - Manual** column. There is a brief description for each dynamic column below:  
  
| Column Name        | How values change | Color status  | Description                                                |
| ------------------ | ----------------- | ------------- | ---------------------------------------------------------- |
| Completed          | By formula        | Colored green | If "Completed - BA" = 0, shows "Completed - Manual" values |
| Completed - Manual | Manually          | Not colored   | Completed minutes filled manually                          |
| Completed - BA     | By formula        | Colored green | Completed minutes from topics in common with BA course     |

### Dashboard and extension
To load the database properly, ensure the data connection in Qlik Sense leads to the correct file location.
It is currently configured in Qlik Sense Desktop to the path ***C:\Downloads\QCC.xlsx***.

Information about [loading data from files](https://help.qlik.com/en-US/sense/February2020/Subsystems/Hub/Content/Sense_Hub/DataSource/load-data-from-files.htm) and [installing extensions](https://help.qlik.com/en-US/sense-developer/February2020/Subsystems/Extensions/Content/Sense_Extensions/CustomComponents/custom-components-installing.htm) can be found at the Qlik Help website. 
