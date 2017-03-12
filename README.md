# trigves-arm
This is a Rapid Application Development tool designed to speed up the work flow by taking out the need to run back and forth from the database. It works on database tables and rows by mapping a multidementional array to the relational database the same way an Orm maps an object. Once installed place the $this_>ArmCheckTables(); function somewhere where it will be ran everytime your page refreshes. If updates are needed it does them automatically. This branch is for custom php projects that run on your home made architectures. I will be updating it with new features and creating other branchs for symfony, laravel and code-igniter.

Due to adding new features to the class last week Im running into new errors. Please give me while to finish edits. Your still welcome to tinker with it though. One new error may erase extra databases so be careful. The other; cause the function checks the count of each table overlooks changes if you erase a row and replace it with another in one refresh. A change like that needs to be done one at a time for the moment. Snce Im fixing that I will add support for chaging names. Thanks.

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
