 * *cat*                                     -> Display whole file
 * *less*                                   -> Display paginate file
 * *head*                                  -> Display 10 rows of top file
		Display 5 lines: **-n 5**        ->            Follow new logs:    **-f**
 * *tail*                                     -> Display 10 rows of bottom file
		Display 5 lines: **-n 5**         ->            Follow new logs:    **-f**
 * *echo*                                  -> Write info to file   
 * *grep*                                   ->  Find a pattern in a file 
   ``cat test.txt | grep ali``   -> use **-i** for both capital and lower case.
 * *sed*                                     -> Update a file by replacing foo by bar                 
   ``sed -i 's/foo/bar/g' test.txt``
 * *diff*                                     -> Compare two text files line by line
 * *cmp*                                   -> Compare two text byte line by byte
 * *sort*                                    -> Sore lines of text files
 * *join*                                     -> Join lines of two files on a common field
 * *cut*                                      -> Split content by some delimiter 
   ``cat test.txt | cut -d ' ' -f2``   ->  Split each line by **space** and display 2nd index of each
 * *awk*                                     -> Like cut with more options      
 * *wc*                                       -> Words, Characters and Lines count
