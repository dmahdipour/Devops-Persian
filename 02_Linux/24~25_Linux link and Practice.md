### Link a file to another place
There are two types of them:
* *Soft-link *(Symbol link): If main file was deleted, it is not working any more. 
     ``ln -s FILENAME LINKENAME``
* *Hard-link* (Like copy but we can change file from both of them): Each file was deleted, nothing will happen to other one.
      ``ln FILENAME LINKNAME``
    