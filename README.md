# trigves-arm
This is a Rapid Application Development tool designed to speed up the work flow by taking out the need to run back and forth from the database. It works on database tables and rows by mapping a multidementional array to the relational database the same way an Orm maps an object. Once installed place the $this_>ArmCheckTables(); function somewhere where it will be ran everytime your page refreshes. If updates are needed it does them automatically. This branch is for custom php projects that run on your home made architectures. I will be updating it with new features and creating other branchs for symfony, laravel and code-igniter.

YOU REALLY HAVE TO WATCH WHEN YOU ARE CREATING YOUR TABLES AND FIELDS  
 * NAMING TWO ROWS THE SAME WILL HALT EXECUTION AND CREATE AN ERROR  
 * NO TWO FIELDS IN A TABLE CAN HAVE THE SAME NAME  
 * NAMING TWO TABLES THE SAME WILL HALT EXECUTION AND CREATE AN ERROR  
 * NO TWO TABLES CAN HAVE THE SAME NAME 
	  
Due to adding new features to the class last week I was running into new errors. When debbugging I realized the new error was not a new error at all but this. If you had named two databases the same they would both be erased. I added new logic for reporting the error. Will uploading it soon. I am also adding logic to report having two rows with the same name. Be back in a minute. Happy Coding!!

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
