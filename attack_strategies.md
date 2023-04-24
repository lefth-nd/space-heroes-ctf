# Attack Strategies

In burpsuite we see a cookie *show_hidden*  
If we set this to true, a new option is revealed in the folder selection  
```flag.txt```  
Since this isn't a folder we should try setting the folder to something else and the file to flag.txt  

We try . for the folder  
Forwarding this packet reveals the flag.  


