Image Category Relevance: 

Business Requirement: 

The GeM portal requires an automated solution to ensure that product images align with the correct 
category specifications. This is critical for maintaining accurate product categorization and improving the 
quality of listings on the platform.  
Currently, the manual oversight process is inconsistent and prone to errors, which affects the reliability 
of the marketplace. The goal is to implement an AI/ML-driven module to automatically verify that 
product images meet the specified category features, thereby enhancing accuracy and reducing manual 
intervention. 

Proposed Solution: 

The solution involves developing a Category Relevance module using a Object detection model, 
specifically leveraging YOLOv8. This module will automate the identification and verification of features 
in product images to ensure that they correspond with the required category specifications.  
By utilizing image annotation data, the system will be able to train a model capable of detecting these 
features in new images, ensuring accurate product categorization on the GeM portal. 

Solution Consumption: 

1. Market Sanitization: 
This process will ensure the quality and accuracy of the marketplace by identifying and removing 
products with images that do not meet category specifications. The module will generate detailed 
reports for GEM SPV, highlighting any discrepancies between the image features and the category 
requirements. 
2. Quality Gate (CMS): 
A quality gate mechanism will be established to prevent sellers from uploading images that do not meet 
the required specifications. Alerts will be generated for GEM SPV and the sellers when an image fails to 
meet the criteria, ensuring compliance with category standards before the product is listed.

Data: 

1. Image Data: Product images sourced from GeM marketplace. The required data can be fetched from 
below tables from the database. 
• inb_variants 
• inb_images 
2. Annotation Data: Images are annotated to identify category-specific features, which are crucial for 
training the object detection model.

Model Methodology: 

1. Image Annotation: 
• Product images are annotated to mark relevant features based on the specific category 
requirements. 
2. Model Training: 
• The annotated data is used to train a YOLOv8 object detection model. This model is refined to 
accurately detect features that are relevant to the category specifications. 
3. Model Evaluation: 
• The trained model is evaluated to assess its accuracy in detecting the annotated features. 
4. Model Testing: 
• The model is tested on new images, where the detected features are compared against the 
Product Data to verify their relevance to the category.

Steps In Model: 

1. Data Collection: Gather image data from GeM source. 
2. Image Annotation: Annotate the images to highlight category-specific features. 
3. Model Training (YOLOv8): Train the YOLOv8 model using the annotated images. 
4. Model Evaluation: Evaluate the model to ensure it correctly identifies the relevant features. 
5. Model Testing: Test the model on new images and compare results with Product data to validate 
category relevance. 
6. Deployment: Created a API to consume the functionality and deployed on the server. 
See the picture below to know the flow of processes in this solution:

![Detection Model Training(YOLO V8 )](https://github.com/user-attachments/assets/1139a474-b9f3-4385-8d5d-a3d00379e130)

Business Value: 

1. Enhanced Accuracy in Categorization: Automating the feature detection and categorization process 
improves the accuracy of product listings, ensuring they are correctly categorized based on their 
images. This reduces the potential for manual errors and oversight. 
2. Improved Marketplace Quality: By ensuring that only accurately categorized products are listed, the 
solution enhances the overall quality and reliability of the GeM platform, fostering better user trust 
and satisfaction. 
3. Efficient Quality Control: The quality gate mechanism prevents non-compliant images from being 
uploaded, streamlining the process of maintaining high standards for product listings. This proactive 
approach minimizes the need for post-upload corrections, improving operational efficiency.

![Example Detection Model Training(YOLO V8 ) images](https://github.com/user-attachments/assets/225448a9-1d7e-45fa-aad6-21df56effe5b)



![Unstructured data analysis - Image Category relevance jpg](https://github.com/user-attachments/assets/e2b4b379-574e-4b6a-bd25-3bd8d21ce71e)

