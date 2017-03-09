# trigves-arm
This is a Rapid Application Development tool designed to speed up the work flow by taking out the need to run back and forth from the database. It works on database tables and rows by mapping a multidementional array to the relational database the same way an Orm maps an object. Once installed place the $this_>ArmCheckTables(); function somewhere where it will be ran everytime your page refreshes. If updates are needed it does them automatically. This branch is for custom php projects that run on your home made architectures. I will be updating it with new features and creating other branchs for symfony, laravel and code-igniter.

INSTALLATION
1) Put class where you can inherit it through extends or include it.
2) Fill in database connection variables,
	private $_db_host;
	private $_db_name;
	private $_db_user;
	private $_db_pass;
3) Call $this->ArmCheckTables()
