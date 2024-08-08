# Ai-Leukemia-Detector
This is an AI that detects signs of leukemia from cells of blood smears.

![out1](https://github.com/user-attachments/assets/d6ba00b0-7a54-48f5-b601-0eef57f8c970)


## The Algorithm

I developed an AI system that runs on the NVIDIA Jetson Nano to analyze blood smear images and detect signs of leukemia. The system processes images through normalization, cell segmentation, and classification using a deep learning model. Trained on datasets, the model differentiates between normal and leukemia cells by examining features such as size, shape, and staining patterns. Using the Jetson Nano’s computing power, the system provides real-time processing and classification, offering prompt and reliable results for medical diagnostics.

![non_cancerous1](https://github.com/user-attachments/assets/460ad88d-193d-4dea-8aa2-80811eeafdcd)
![non_cancerous](https://github.com/user-attachments/assets/c6779263-e388-422b-b54a-9b97ffc6fb5e)
![cancerous3](https://github.com/user-attachments/assets/e47b3362-276d-4474-9362-bcca4fdaa8c8)
![cancerous2](https://github.com/user-attachments/assets/756d12da-b788-4bff-b778-6a6371c6f814)
![cancerous1](https://github.com/user-attachments/assets/dd11dcae-268c-4eb7-857d-9fdef6047386)

![cancerous](https://github.com/user-attachments/assets/cdaba2e6-b4b4-4263-adb0-6729cd89f2d4)




## Running this project
 1. Setup your Jetson Nano and Install VScode
2. Connect Jetson Nano onto your computer hotspot. Write down your Jetson Nano IP address for later use
3. Connect your VScode to your Jetson Nano using Connect Host and ssh nvidia@IPAddress
4. Open the NVIDIA home folder
5. Open the terminal and use cd jetson-inference/python/training/classification to enter the needed directory
6. Use NET=models/ai_final and DATASET=data/ai_final to set NET and DATASET for later reference
8. Run the model using imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/(cancerous / non_cancerous)/(image name).jpg (output image name).jpg IMAGE_NAME with the name of your image and IMAGE_OUTPUT_NAME with the name of what you want the output image to be.
9. Clcik on the output image to see the result!

(video link)
z
(https://www.youtube.com/watch?v=rvYWbHV3xus)
