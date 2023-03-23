#  Project Name: MY-2-OF-MY-30-DAYS-DATA ANALYSIS


# Project Objective: Learning how to scrape a COVID-19 dataset from Github using Microsoft 

---
# Data Sourcing
Data source was from the John Hopkins Hospital Covid-19 dataset file:
CSSEGISandData/COVID-19/blob/master/csse_covid_19_data/csse_covid_19_time_series

# Steps Taken and Cleaning
STEP 1: ON the CSSEGISandData of John Hopkins Hospital i choosed the covid_19_time_series file and open it to get more datasets for my work.
        the first data i choose was the global confirmed case of covid_19. I choose the raw file instead of downloading it since i wanrt to work on a live field/daily           update file. 
        
STEP 2: I copied the Url address and open my Excel worksheet. In Excel click on New Query and then from source click on from web, then input the URL address into the           box provided and laod it into the Power Query. Transform the data first so the cleaning and other processes can be done in the Power Query,

STEP 3: I made changes to my Confirm case dataset such as 
A) changing the header column
B) Changing the data types 
C) My data was a WIDE DATA(many columns than rows) to change this i highlighte the first 4 colums i had and right click a chose "unpivot other columns" this shorten the colums.
D) Names of two headers where changed to the appriotr names i.e Attributes was changed to Date and Value was changed to Confirm.

STEP 4: I duplicated the Confirm case in Power Query dataset and renamed te new data as Death case.This duplicated data still has the Confirm case information in it so to change it i did the following
A) Go back to the data source in Github and click on the Confirm Death cases chose the raw file and copy the URL address as you did in the Confirm cases. 
B) On the right hand side of my worksheet in Power Query where you will find the steps of the changes made click on the gear box beside my source step and in the url box replace the Confire case URL address with the Death case URL address and load. What this does is to change the info in the Death case to its original information. There was no neeed to repeat any changes cause due to the duplicate every source changes you did in the first dataset will be repeated in the seconfd data set.

STEP 5: Repeat the same steps as you did above for the third dateset you need by duplicating the data of Death cases and going back to your data source and copy the raw URL address for Recovered cases and inputing it in your soure step and load.  

# Merging of the Datasets
STEP 1: Click on the confirmed case query at the right hand side, On the home tab of Power Query click on the drop down arrow beside the Merge Queries tab and choose NEW QUERIES.

STEP 2: This will bring a Box with your Confirm Cases figure, below this therer is another empty box with the write up NO PREVIEW click on the formula box above this and choose Death Case and ok it
A) On the confirm cases preview highlight the colums you want to merge together( this are colums that have the same figures or the same data as your other columns), repeat this same step with that of the Death cases preview. Make sure there is no synthax error showing after his process clic on ok.
B) After you ok this a box appear requesting for PRIVACY LEVELS  here you will input the URL adress of the data source and then make this PUBLIC, click on save nad continue your merging by clicking ok.
C) This creates another Query known as MERGE 1, this has the Confirm and Death cases merge as one.   
D) Click on the MERGE 1 dataset and on the home tab click on MERGE QUERIES and not MERGE NEW QUERIES and repeat the same step as above but in this case we are choosing the RECOVERED cases file to merge with the death and confirm cases.
E) the header of Death cases and Recovered cases has a double arrow sigh beside them and there figures are showing zero to remove this click in the double arrow sigh an uncheck all the box, but check only the box that represent your header name.
F) Click on close and load to create this in Excel

# Problem Encountered and Overcoming them
1) In Microsoft 365 when you load from the web when in the data tab it takes you directly to where you will input the URL address and load it into Powewr Query but this is not the same as Microsoft Excel. 
In Microsoft Excel you have to go to the Data tab and click on New Query and then choose the source( from the web) and then input the URL address and load it to Power Query.

2) Step are important in merging your dataset if you input a wrong step from your previous step this will result to a sythax error again and again.
