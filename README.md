# Code for  generating Qr Code 

import qrcode
from PIL import Image 


san = qrcode.QRCode(version=1,
                    error_correction=qrcode.constants.ERROR_CORRECT_H,
                    box_size =10, border =4  )

san.add_data("https://www.linkedin.com/in/sanjay-kumar-126261329/")
san.make(fit = True)

image = san.make_image(fill_color = "black", back_color="white")
image.save("Linked_profile.png")
