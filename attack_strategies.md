# Attack Strategies

In burpsuite we see a cookie *show_hidden*  

![Screenshot 2023-04-23 103047](https://user-images.githubusercontent.com/74050386/233902549-ca16a378-d4d1-4bb6-9741-5ce659c6e8c1.png)

If we set this to true, a new option is revealed in the folder selection  
```flag.txt```  
Since this isn't a folder we should try setting the folder to something else and the file to flag.txt  

We try . for the folder  

![Screenshot 2023-04-23 103108](https://user-images.githubusercontent.com/74050386/233902584-5e6fa1ef-9caa-4bdd-ae19-ef1006e148ed.png)

Forwarding this packet reveals the flag.  

![Inkedimage](https://user-images.githubusercontent.com/74050386/233902701-304647fb-eeae-4e3e-926b-bc71b318ccd6.jpg)

