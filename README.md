# Amini_Seth
# NDVI Plot

![image](https://github.com/sethgis/Amini_Seth/assets/50513411/67048f4c-111d-4672-b38d-f9beb5481adf)

Geo-backend_workflow
The main code is located at the original_code.py file, it encapsulates all the automated workflow for the following explanation.
## Data pulling - It applies non-GEE data pulling, and pulls data from the AWS Open data hub, through an API managed by element 84
The API pulls sentinel scene data when passed with start and end dates. I downloaded the same image as acquired in the shared folder

The available APIs pull data in Cloud Optimized Geotiffs (COG) format, which enables us to use resources such as array computation in virtual machines such as Dask.

After pulling the data, the workflow automatically computes NDVI and NDWI for the specific scenes subsetted based on input geojson, plots the NDVI files and saves it into a folder.
The code also saves an RGB tile of the first scene into a folder.

Besides this, the code saves the NDVI tiff files into a folder i.e. projected tiff files and un-projected tiff files.

Projected files are saved into a folder indicated projected. The indices are also plotted and saved into a folder known as sentinel. The folder also houses the RGB tile extracted from the analysis.

Depending on the number of scenes, the code may take longer to process, and thus it is advisable to pass in at least weekly dates for faster processing.

If given time, I could easily transform the workflow into a functional API, deploy with Kubernetes for scalability of the application, and provide a rapid solution to the organization's needs. Please reach out in case of any queries.

The reason why sentinel hub was not used: Sentinel hub was recently acquired by a Planet tech company, and  since Amini is a tech company in the same space, for the security of vital processes used internally, the only secure option to pull data is through AWS who are not in the tech space and are not competitors.
