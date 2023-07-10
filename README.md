# Qr_code_project




This project demonstrates how to generate a QR code for a YouTube video link using the qrcode library in Python. The generated QR code is saved as an image file.



# Prerequisites


Python 3.x


qrcode library


PIL (Python Imaging Library) library



# Installation




Make sure you have Python 3.x installed on your system. If not, you can download and install it from the official Python website: https://www.python.org/downloads/



Install the required libraries by running the following command in your terminal:


**pip install qrcode pillow**



# Usage



Import the necessary libraries:


import qrcode


from PIL import Image


**Create a QRCode object with the desired settings:**


qr = qrcode.QRCode(
    version=1,
    error_correction=qrcode.constants.ERROR_CORRECT_H,
    box_size=20,
    border=3,
)


# Add the data (YouTube video link) to the QR code:


qr.add_data("https://www.youtube.com/watch?v=FOGRHBp6lvM&list=PLjVLYmrlmjGfAUdLiF2bQ-0l8SwNZ1sBl")


#  Generate the QR code image:



qr.make(fit=True)


img = qr.make_image(fill_color="blue", back_color="yellow")


#  Save the QR code image as a file:



img.save("video_youtube.png")



# Execution

Save the provided code in a Python file, e.g., generate_qr_code.py.



# Run the Python script:



python generate_qr_code.py


This will generate a QR code image named video_youtube.png in the same directory.



**Further Information**



For further information on the qrcode library, please refer to the official documentation: https://pypi.org/project/qrcode/


For further information on the PIL (Python Imaging Library) library, please refer to the official documentation: https://pillow.readthedocs.io/en/stable/

