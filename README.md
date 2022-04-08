# Login2Xplore JsonPowerDB Project

[Documentation Link](http://login2explore.com/jpdb/docs.html)

[Project Main Page Link](https://philomath242.github.io/Login2Xplore-Project/)

## A student database project using JsonPowerDB for performing Create, Read, Update, Delete  basic operations.
### Feel free to fork the repository and tinker with the code
### About JsonPowerDB:

- JsonPowerDB is a Real-time, High Performance, Lightweight and Simple to Use, Rest API based Multi-mode DBMS. 
- JsonPowerDB has ready to use API for Json document DB, RDBMS, Key-value DB, GeoSpatial DB and Time Series DB functionality.
- JPDB supports and advocates for true serverless and pluggable API development.

### Benefits of using JsonPowerDB

- Fast and easy database management with extensive functions
- It helps in quick development with minimal coding, reducing development cost.
- Schema-free models allow for flexible structuring of data
- It is built on top of one of the fastest and real-time data indexing engine - PowerIndeX.
- It is low level (raw) form of data and is also human readable.


### Release Notes

- Prototype project with minimal error-handling
- getRecordNumberByKey() is a function to get record number by a defined key
- Display of creation time is also added for extra functionality
- Updates the record even if at least one field to update is provided
- Primary key apart from record number is the student's roll number

### Table of contents

#### Main Page

The homepage for the student database where an user can be redirected to the respective operation pages based on the link the user clicks on. 

#### Register Student Details Page

Register Student Details Page is where the student form where student data is entered in the input fields. The form data is then validated using defined function `validateAndGetFormData()`. If any required field is empty, then it alerts the user to fill in the field. With validated data being converted to `JSON` string, a `PUT` request is sent to the `JPDB` api for handling insertions. On successfull insertion, user is alerted the success message before resetting the form for other records to be inserted. 

#### Get Student Details Page

Get Student Details Page allows the user to get record column details based on user roll number. It displays the fetched data in a div container which is made visible using `display:block` along with the creation date and time. It has a `Clear` hyperlink to clear the form and reset the div container to `display:none`.

####  Update Student Details Page

Update Student Details Page can be used to update existing records in the relation. It requires the primary key which is roll number. A new custom function `getRecordNumberByKey(roll)` was created to get record number based on roll number of a student. The functional scope of this is limited to change any field other than the primary key which is thought of to be the roll number in this case. If all fields are left empty, it prompts the user to enter proper data to be updated. At least one field other than the roll number is to be given to update. The function `validateAndGetFormData()` is modified to perform an action of filtering those keys inside the `JSON` which have empty string values to prevent those fields from updating unnecessarily.

####  Delete Student Details Page

Delete Student Details Page can be used to delete records in the relation. THe form field asks for roll number of the user and upon clicking `Delete`, a prompt is shown to user to confirm the deletion of the record associated with the provided roll number. On confirming it, the record is successfully deleted, while on cancelling the request the form is cleared without sending any request. 

### Illustrations



![Main Page](https://github.com/philomath242/Login2Xplore-Project/blob/9ec3046d2214e060130b3c4bb4763ebdb92cbb75/Snaps/mainpage.jpg)
#####  Main Page

![Register Student Details Page](https://github.com/philomath242/Login2Xplore-Project/blob/9ec3046d2214e060130b3c4bb4763ebdb92cbb75/Snaps/registerstudentdetailspage.jpg)
#####  Register Student Details Page

![Get Student Details Page](https://github.com/philomath242/Login2Xplore-Project/blob/9ec3046d2214e060130b3c4bb4763ebdb92cbb75/Snaps/getstudentdetailspage.jpg)
#####  Get Student Details Page

![Update Student Details Page](https://github.com/philomath242/Login2Xplore-Project/blob/9ec3046d2214e060130b3c4bb4763ebdb92cbb75/Snaps/updatestudentdetailspage.jpg)
#####  Update Student Details Page

![Delete Student Details Page](https://github.com/philomath242/Login2Xplore-Project/blob/9ec3046d2214e060130b3c4bb4763ebdb92cbb75/Snaps/deletestudentdetailspage.jpg)
#####  Delete Student Details Page


![Stored Records in Relation in Database](https://github.com/philomath242/Login2Xplore-Project/blob/50ec1284f16a128130c13bde6e01be3d0be76d8f/Snaps/database.jpg)
#####  Stored Records in Relation in Database





###  ________________________________________________________
# Site Structure
`index.html`         #       Main Page  <br />
  ├─ `studentform.html` #       Register Student Details Page   <br />
  ├─ `readstudent.html`- #       Get Student Details Page   <br />
  ├─ `updatestudent.html` - #       Update Student Details Page   <br />
  ├─ `deletestudent.html`#       Delete Student Details Page   <br />
  
  ###  ________________________________________________________




### Scope of functionalities

#####  It is created with my college in mind with just three fields namely student's roll number, student's name and student's email address, but the functional scope can be extended to allow different student databases with multiple fields.


