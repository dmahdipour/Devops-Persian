* Avoid to give/take extra access to/from a users/admins.
* Some file for storing users, groups, passwords, etc. and for working with accesses:
	* */etc/shadow*
	* */etc/passwd*
	* */etc/group*
	* */etc/sudoers*     
		**Note:** Even root users just can read it and you have to change its access then edit the contents. Use "vis" for be sure about its syntax and configs. You can config it for special user to access just some commands.
* List of some commands to work with them:
	* *addusr*
	* *userdel*
	* *passwd*
	* *last*                        ``#last loggined user``
	* *id*                           ``#current user info``
	* *sudo*
	* *w*
	* *whoami*
