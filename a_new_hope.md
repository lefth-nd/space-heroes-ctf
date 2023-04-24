# A New Hope

We start with a .pptx file that has three images. Moving two images out of the way reveals the third image, yet it is broken.  
Changing the file to a .zip allows us to inspect the image closer.  

Dropping the broken image into a hex editor we see a broken JFIF header.
Repairing this header with:  

```FF D8 FF E0 00 10 4A 46 49 46 00 01```

This reveals the image with the flag.
