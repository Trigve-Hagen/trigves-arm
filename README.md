# trigves-arm
This is a Rapid Application Development tool designed to speed up the work flow by taking out the need to run back and forth from the database. It works on database tables and rows by mapping a multidementional array to the relational database the same way an Orm maps an object. Once installed place the $this_>ArmCheckTables(); function somewhere where it will be ran everytime your page refreshes. If updates are needed it does them automatically. This branch is for custom php projects that run on your home made architectures. I will be updating it with new features and creating other branchs for symfony, laravel and code-igniter.

YOU REALLY HAVE TO WATCH WHEN YOU ARE CREATING YOUR TABLES AND FIELDS  
 * NAMING TWO ROWS THE SAME WILL HALT EXECUTION AND CREATE AN ERROR  
 * NO TWO FIELDS IN A TABLE CAN HAVE THE SAME NAME  
 * NAMING TWO TABLES THE SAME WILL HALT EXECUTION AND CREATE AN ERROR  
 * NO TWO TABLES CAN HAVE THE SAME NAME 


<span style="color:#f00;">Still erroring on localhost when there are two databses only and you delete one. Sometimes both are deleted. Im working on a fix.</span>

Due to adding new features to the class last week I was running into new errors. When debbugging I realized the new error was not a new error at all but this. If you had named two databases the same they would both be erased when dropping a table. I added new logic for reporting the error. I also adding logic to report having two rows with the same name and errors and messages for everything else. PLease be carefull anyways. I take no responsibility for lost data! Use at your risk. If I have no new problems to report in the next month of developing with it than it is done. Happy Coding!!  

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
