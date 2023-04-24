# A New Hope

We start with a .pptx file that has three images. Moving two images out of the way reveals the third image, yet it is broken.  
Changing the file to a .zip allows us to inspect the image closer.  

Dropping the image into a hex editor we see a broken JFIF header.
Repairing the header with:  

```FF D8 FF E0 00 10 4A 46 49 46 00 01```

Reveals the image with the flag.

![Inkedimage1](https://user-images.githubusercontent.com/74050386/233901438-b966166b-a089-4eff-ac06-9c398b5c025a.jpg)
