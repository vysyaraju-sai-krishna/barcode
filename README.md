we are going to write a short script to generate barcodes using Python. We'll be using the python-barcode module which is a fork of the pyBarcode module. This module provides us the functionality to generate barcodes in SVG format. 
Pillow is required to generate barcodes in image formats (such as png or jpg).

Modules required :

python-barcode: This module is used to create bar codes as SVG objects. It provides us the power to create different standard types of barcodes such as EAN-8, EAN-13, EAN-14, UPC-A, JAN, ISBN-10, ISBN-13, and many more.
To install this module type the below command in the terminal.


pip install python-barcode  


Pillow: This is used to create the barcodes in the image format. To install this module type the below command in the terminal.
pip install pillow


Here, we are going to generate a barcode in the EAN-13 format. First, let's generate it as an SVG file.



from barcode import EAN13
number = '5901234123457'
my_code = EAN13(number)
my_code.save("new_code")


Now, let's generate the same barcode in PNG format.


# import EAN13 from barcode module
from barcode import EAN13
from barcode.writer import ImageWriter
number = '5901234123457'
my_code = EAN13(number, writer=ImageWriter())
my_code.save("new_code1")
