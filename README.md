# trigves-arm
This is a Rapid Application Development tool designed to speed up the work flow by taking out the need to run back and forth from the database. It works on database tables and rows by mapping a multidementional array to the relational database the same way an Orm maps an object. Once installed place the $this_>ArmCheckTables(); function somewhere where it will be ran everytime your page refreshes. If updates are needed it does them automatically.

YOU REALLY HAVE TO WATCH WHEN YOU ARE CREATING YOUR TABLES AND FIELDS
 * WHEN FIRST PUT INTO USE IT WILL ERASE ANYTHING DONE BEFORE IT AND CREATE A SAMPLE USER DATABASE
 * NAMING TWO ROWS THE SAME WILL HALT EXECUTION AND CREATE AN ERROR  
 * NAMING TWO TABLES THE SAME WILL HALT EXECUTION AND CREATE AN ERROR  
 * DATABASES SOMETIMES ONLY ALLOW A TOTAL NUMBER OF VARCHAR CHARACTERS IN A TABLE - THE ARRAY WON'T UPDATE THE DATABASE IN THIS CASE  
 * WHEN QUERYS ARE RAN ON THE DATABASE THE DATABASES TURNS UPPERCASE TO LOWER CASE. THEN WHEN CHECKED AGAINST - $_tablesArray (UPPER CASE) AGAINST THE DATABASE ARRAY(LOWWER CASE) IT RETURNED NOT IN THE ARRAY AND DELETED THEM BOTH. - users_c3p0r2d2007OG - has to be users_c3p0r2d2007og

I take no responsibility for lost data! Use at your risk. Happy Coding!!  

INSTALLATION  
1) Put class where you can inherit it through extends or include it.  
2) Fill in database connection variables,  
	private $_db_host;  
	private $_db_name;  
	private $_db_user;  
	private $_db_pass;  
3) Call $this->ArmCheckTables();


3/10/2017 - updates  
* added support for adding multiple rows in a table that are next to each other.  
* added support for droping unneeded tables - just erase them from the array.  

3/13/2017 - updates  
* added support for changing row names  
* added error reporting
