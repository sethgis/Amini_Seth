# Amini_Seth
# NDVI Plot

![image](https://github.com/sethgis/Amini_Seth/assets/50513411/67048f4c-111d-4672-b38d-f9beb5481adf)

Geo-backend_workflow
The main code is located at the original_code.py file, it encapsulates all the automated workflow for the following explanation.
## Data pulling - It applies non-GEE data pulling, and pulls data from AWS Open data hub , through a GEO -API managed by element 84
The API pulls sentinel scenes data when passed with start and end dates. I downloaded the same image as acquired in the shared folder

The available APis pulls data in Cloud Optimized Geotiffs (COG), which enables us to use resources such as array computation in virtual machines such as Dask.

After pulling the data, the workflow automatically computes NDVI and NDW for the specific scenes, plots the NDVI files and saves it into a folder.
The code also daves an RGB tile of the first scene into a folder.

Besides this, the code saves the NDVI tiff files into a folder i.e projected tiff files and un-projected tiff files.

Depending on the number of scenes, the code may take longer to process, and thus it is advisable to pass in atleast weekly dates for faster processing.

If given time, I could easily transform the workflow into a functional API, deploy with kubernetes for scalability, and provide as a rapid solution to the organisation 
needs. Please reach out incase of any querries.
