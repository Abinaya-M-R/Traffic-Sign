# Traffic-Sign

Step 1: Install Required Libraries
You begin by installing two Python libraries:

OpenCV: Used for reading and processing images.

Scikit-learn: Used for machine learning tasks like computing similarity between data points.

Step 2: Import Libraries
You import all the necessary libraries:

cv2 (OpenCV): For image handling.

NumPy: For array manipulations.

Google Colab’s files module: To upload and download files in the notebook.

Matplotlib: To display images.

cosine_similarity from scikit-learn: To compare images based on their feature similarity.

datetime: To generate timestamps.

Step 3: Define Image Preprocessing
You define a function that:

Reads the image from disk.

Resizes it to 64x64 pixels.

Converts it to grayscale.

Flattens it into a 1D array (vector) so it can be compared with other images.

This preprocessing ensures all images have the same format and size for accurate comparison.

Step 4: Upload 10 Reference Images
You ask the user to upload exactly 10 images, each representing a different traffic sign. If fewer or more than 10 are uploaded, the code stops with an error. Then, each image is preprocessed using the function from Step 3 and stored in a list.

Step 5: Assign Labels to Images
You manually assign a label (like "Stop", "Yield", etc.) to each of the 10 uploaded images. This step tells the system which image corresponds to which traffic sign.

Step 6: Display Label Mappings
You print out a list that shows which uploaded image corresponds to which traffic sign label. This is helpful for verifying the mapping.

Step 7: Upload a Test Image
You ask the user to upload one image that needs to be classified. The system ensures only one image is uploaded. This test image is then preprocessed just like the reference images.

Step 8: Compare Images
You use cosine similarity to measure how similar the test image is to each of the 10 reference images. The index of the most similar reference image is found, and the label associated with it is chosen as the predicted traffic sign.

Step 9: Show Prediction
You print the predicted traffic sign and the similarity score (a number between 0 and 1 showing how confident the match is — closer to 1 means more similar).

Step 10: Display Test Image
You show the uploaded test image along with the predicted label using a plot. This gives a visual confirmation of the prediction.

Step 11: Save Results
You write the results — including reference mappings and prediction details — into a text file. The filename includes the current date and time to make it unique.

Step 12: Download Text File
Finally, you automatically trigger a download of the text file so the user can keep a record of the result.

