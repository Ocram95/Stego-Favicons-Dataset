# Stego-Favicons-Dataset

This repository contains 2 datasets of 32x32 pixels favicons/images modified via the LSB steganographic technique to contain different malicious payloads, i.e., PHP scripts and URLs. 
The payloads are selected to fit in the first bit of each color channel, i.e., max 32x32x3 bits.  
 

The original images are borrowed from the [CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html) public available dataset.
The tool used for the LSB steganographic technique is the [LSB-Steganography](https://github.com/RobinDavid/LSB-Steganography).
The PHP scripts are borrowed from the [PHP-Malware-Collection](https://github.com/marcocesarato/PHP-Malware-Collection) (28 different scripts).
The malicious URLs are borrowed from the [URLhaus](https://urlhaus.abuse.ch) collection.


In particular:
- Dataset1: 360.000 images. 
	- clean: 60.000 legitimate images from the CIFAR-10 dataset;
	- LSB_stego_php: 60.000 images embedded with suitable PHP scripts (obtained by combining each legitimate image with 1 PHP script);
	- LSB_stego_url: 240.000 images embedded with URLs (obtained by combining each legitimate image with 4 different URLs).

The PHP scripts pool is composed of 28 different scripts whereas the URLs are 1.000, split into 500 IP addresses and 500 DNS entries.

- Dataset2: 90.000 images.
	- clean: 15.000 legitimate images from the CIFAR-10 dataset;
	- LSB_stego_php_b64: 15.000 images embedded with suitable base-64 PHP scripts (obtained by combining each legitimate image with 1 base-64 PHP script);
	- LSB_stego_url: 60.000 images embedded with unseen URLs (obtained by combining each legitimate image with 4 different URLs).


The base-64 PHP scripts pool is composed of 21 different scripts whereas the URLs are 1.000, split into 500 IP addresses and 500 DNS entries.
# Detection
A Deep Learning approach has been implemented for the detection and the classification of the Stego-Favicons-Dataset. You can find more information in the respective [Github repository](https://github.com/massimo-guarascio/FaviconStegoDetection).

# References
Soon

# Acknowledgements 
This work was partially supported by the Horizon 2020 Program through [SIMARGL] (https://simargl.eu/) H2020-SU-ICT-01-2018, Grant Agreement No. 833042, and [CyberSec4Europe] (https://cybersec4europe.eu/), EU  H2020-SU-ICT-03-2018, Grant Agreement No. 830929.
