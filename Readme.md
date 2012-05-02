Klint Instant Messanger
=======================

A minimal server for a terminal chat application that you can pipe into

Licence
-------

<pre>
# ----------------------------------------------------------------------------
# "THE BEER-WARE LICENSE":
# Frank Ellis wrote this file. As long as you retain this notice you
# can do whatever you want with this stuff. If we meet some day, and you think
# this stuff is worth it, you can buy me a beer in return.
# ----------------------------------------------------------------------------
</pre>

Setup
-----

* Put the files *kim_server* and an empty file called *kim.dat* on your web server
* Set the $url variable in the file *kim* to be the url of your web server
* Share the client with your friends

Usage
-----
	PIPE | ./kim ARGS 
		
 		OR
 	
	./kim ARGS		
 	
      	ARGS:
       -w MESSAGE => write message
       -r1        => read messages
       -l LIMIT   => the number of messages to limit to
       -c1        => clear history
       -h1  	  => show this help	

Examples
--------
	
* Send a message:

 		./kim -w 'Something to say'

* Read the last five messages:

		./kim -r1 -l5
	
* Pipe echo into KIM:

		echo 'Somthing to say' | ./kim

* pipe cat into KIM:

		cat file.txt | ./kim

* Write the last message to file:

		./kim -r1 -l1 >file.txt
	
* Clear the history [*]:

		./kim -c1

[*]: All messages go to the same chatroom and 'clear' will empty the chatroom history entirely
