# JDCRP Automatic Document Scanner built in Python using OpenCV with Interactive Capabilities

![JDCRP](https://media-exp1.licdn.com/dms/image/C4D0BAQE3Pdg723dnkg/company-logo_200_200/0/1604570886991?e=2159024400&v=beta&t=tnNA8fTWZv3J2T7GjKBGok7pqBi_1BWofa1SEBorouk)

The scanner takes a poorly scanned image, finds the corners of the document, applies the perspective transformation to get a top-down view of the document, sharpens the image, and applies an adaptive color threshold to clean up the image.

This project makes use of the transform and imutils modules from pyimagesearch (which can be accessed [here](http://www.pyimagesearch.com/2014/09/01/build-kick-ass-mobile-document-scanner-just-5-minutes/)). The UI code for the interactive mode is adapted from `poly_editor.py` from [here](https://matplotlib.org/examples/event_handling/poly_editor.html).

* You can manually click and drag the corners of the document to be perspective transformed:
![Example of interactive GUI](https://github.com/andrewdcampbell/doc_scanner/blob/master/ui.gif)

* The scanner can also process an entire directory of images automatically and save the output in an output directory:
![Image Directory of images to be processed](https://github.com/andrewdcampbell/doc_scanner/blob/master/before_after.gif)

#### Here are some examples of images before and after scan:
<img src="https://github.com/elevin04/JDCRP-Document-Scanner/blob/master/examples/input/cell_pic.jpg" height="450"> <img src="https://github.com/elevin04/JDCRP-Document-Scanner/blob/master/examples/output/cell_pic.jpg" height="450">

<img src="https://github.com/elevin04/JDCRP-Document-Scanner/blob/master/examples/input/receipt.jpg" height="450"> <img src="https://github.com/elevin04/JDCRP-Document-Scanner/blob/master/examples/output/receipt.jpg" height="450">

<img src="https://github.com/elevin04/JDCRP-Document-Scanner/blob/master/examples/input/math_cheat_sheet.JPG" height="450"> <img src="https://github.com/elevin04/JDCRP-Document-Scanner/blob/master/examples/output/math_cheat_sheet.JPG" height="450">

<img src="https://github.com/elevin04/JDCRP-Document-Scanner/blob/master/examples/input/dollar_bill.JPG" width="350"> <img src="https://github.com/elevin04/JDCRP-Document-Scanner/blob/master/examples/output/dollar_bill.JPG" width="350">


### Usage
```
python scan.py (--images <IMG_DIR> | --image <IMG_PATH>) [-i]
```
* The `-i` flag enables interactive mode, where you will be prompted to click and drag the corners of the document. For example, to scan a single image with interactive mode enabled:
```
python scan.py --image sample_images/desk.JPG -i
```
* Alternatively, to scan all images in a directory without any input:
```
python scan.py --images sample_images
```
