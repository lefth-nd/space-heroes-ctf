## I OFTen See Star Wars

Unzipping the Aurebesh file, we get 8 .otf font files.  
The first clue is in '1-Aurebesh Bold Italic' at 01F0  
Scrolling down a bit in a hex editor, the string *hctf* jumps out.  

At the same position in the next .otf we get the next 4 bytes of the flag.  

Putting all of these together in order, we get...  

``` hctf th3r _1s_ lway _s0m _h0p _4r0 nd} ```

Each is missing one character. Where is it hiding?  
After some detailed forensic analysis *frantically scrolling*  
The 's' for the first 4 bytes is located at 0140, 12 bytes in.  
Subsequently, the rest of the missing characters are at that position in each file, in order.  

``` s { 3 a s e 3 u ```

Giving us the flag.
