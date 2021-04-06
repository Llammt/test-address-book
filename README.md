# test-address-book
Temporary test project

The main goal of this development is show to owners of projects how the candidat can make the dev process.

# Project address book

The simple task save and maintenance the contacts.

Contact:
- first name
- second name
- birthday
- phone number
- email

Input:
- from terminal
  - ask user for entering each part
  - quit after entering one contact
  - introduce unqiue ID of contact
  - edit by exactly ID or phone number or email

Output:
- show list
  - full
    - output only desired parts, for example first and last name only
  - filtered
    - can be filtered by any part of entity
    - or filtered by definitely part let say by phone number only
  - sorted
    - sort by any part
 
 Interface:
   - command line
     - `--show` show list of contacs
       - `--filter` add filters:
         - `--filter=all` just try filter all parts last argument is a sub-string for search
         - `--filter={email|phone|fname|lname|birthday}` search by parts
         - `--filter=birthday today` show all contacts which have birthday today
     - `--new` enter to interactive input, part by part until all parts will be ready
     - `--add --fname={FNAME} --lname={SNAME} --phone={PHONE} --email={EMAIL} --birthday={BIRTHDAY_DATE}` just add new record fomr command line without any questions, should reject if the record exists

Technical details:
- make the alpha branch for showing final results
- input/output made by std::iostream using std::cin and std::cout
- error messages shoul output to std::cerr
- processing the command line arguments should be implemented by boost::program_options
- all in-memory storage using std containers
- all sorting and filtering using std algorithm
- save/restore data to/from CSV file
- make backup before apply any changes
- add couple unittests using gtest library
- project shuld be build using cmake
- show us the best software engeneering skills
  - good OOP design
  - divide by modules
  - using a couple of software design patterns
- document all code in dpxygen style
