# -fomo_face_detection
TingML machine learning model using FOMO for MCU

The model training can be found at: 
https://studio.edgeimpulse.com/public/1100575/live 

Targeted devices: IXAO ESP32S3 & Portenta H7 

  - Time inference for IXAO ESP32S3 (Theoretical: 877 ms && experimental: 2200 ms) 
  - Time inference for Portenta H7 (Theoretical: 57 ms && experimental: 65 ms)

<img width="1280" height="960" alt="WhatsApp Image 2026-08-31 at 4 13 41 AM" src="https://github.com/user-attachments/assets/7d16239f-0e72-45b7-8d08-70f06d8a5782" />


# Results 
           - IXAO ESP32S3
<img width="549" height="47" alt="IXAO" src="https://github.com/user-attachments/assets/1199bf99-e5ac-49ed-9ea9-a41b98d5d311" />

           - Portenta H7
  <img width="434" height="83" alt="portentaH7" src="https://github.com/user-attachments/assets/bb6d6ce7-4d8d-4666-8329-21f832ef78d4" />


# Important tips about XIAO before uploading the code: 
       1. Navigate to file ei_classifer_config.h located inside the installed library files, and turn off ESP NN acceleration by adding 
                #define EI_CLASSIFIER_TFLITE_ENABLE_ESP_NN 0 on line 82 
       2. Setting Tools → PSRAM from disabled to OPI PSRAM

# Recommendations and Conclusions: 
 - XIAO ESP32S3 operates at slow inference time, and not suitable for real application.
 - Portenta H7 has good performance, but it comes with higher cost. 
 - Collect images using the same device used for the deployment part for better final results. 
