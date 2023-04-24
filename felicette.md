## Felicette


Starting with a .pcap we note the file name *chall.jpg.pcap* hinting at a jpg buried within the pcap  
Further inspection shows data for packets 7 to 10 spelling out JFIF.  

```
0000   45 00 00 1d 00 01 00 00 40 01 a9 c4 0a 9a 04 75   E.......@......u
0010   c0 a8 01 64 08 00 ad ff 00 00 00 00 4a            ...d........J

0000   45 00 00 1d 00 01 00 00 40 01 a9 c4 0a 9a 04 75   E.......@......u
0010   c0 a8 01 64 08 00 b1 ff 00 00 00 00 46            ...d........F

0000   45 00 00 1d 00 01 00 00 40 01 a9 c4 0a 9a 04 75   E.......@......u
0010   c0 a8 01 64 08 00 ae ff 00 00 00 00 49            ...d........I

0000   45 00 00 1d 00 01 00 00 40 01 a9 c4 0a 9a 04 75   E.......@......u
0010   c0 a8 01 64 08 00 b1 ff 00 00 00 00 46            ...d........F
```

This means that if we extract the data from each ICMP packet into a another file, we should get an image.  
Time to break out some python.

```
from scapy.all import *
from io import BytesIO
from PIL import Image

# Open the PCAP file for reading
pcap_file = "chall.jpg.pcap"
packets = rdpcap(pcap_file)

# Loop through each packet in the file
for packet in packets:
    # Extract data from the packet
    data = packet.load

    with open("chall.jpg", "ab") as f:
        f.write(data)
```

This script loops through each packet and writes the data to a chall.jpg file.  
Since the script takes longer than 5 mins to exectute, there's probably a more efficient way to do this.  
After some waiting, we get the flag.  
