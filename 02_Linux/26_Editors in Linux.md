There are 2 type of editors and you have to be expert in one for each type (Choose the most popular of them):
* *GUI*: **vscode**, notepad, gedit, sublime
* *CLI*: **vim**, nano, vi

**VIM** use *Esc* key to get out of a mode
*  *Command Mode*
	* Go to line by Line number               -> :44
	* Search a text                                     -> /test         -> use **n** to go to next
	* Replace a text1 by other text2        -> :%s/text1/text2/g
	* Head of file                                         -> gg
	* End of file                                            -> G
	* Copy whole line                                  -> yy              -> ex: use **y3y** to copy three line
	* Cut whole line                                     -> dd              -> ex: use **d3d** to cut three line
	* Paste that line                                     -> p
	* Undo changes                                     -> u                 -> use **U** to undo to origin content
	* Redo changes                                     -> r                  -> use **R** to undo to origin content
	* Past clipboard in good way               -> :set paste
* *Insert Mode
	* Go to Cursor place by **INSERT** button or **i** key
	* Go to next character of Cursor place by **INSERT** button or **i** key
* *Save Mode*
	* Write                                                         -> w
	* Quit                                                           -> q            without saving:  q!
	* Write and Quit                                         -> wq     or      x
	