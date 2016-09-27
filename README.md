# DARPDATASET
Dataset for static Dial-a-ride problem without ride-sharing

-----------------------------------

This repository contains  datasets for static Dial-a-Ride Problem (DARP) without ride-sharing. DARP consists of both spatial (space related)
and temporal (time related) factors. These datasets can be used to analyze the impact of spatial  and temporal  factors on 
static DARP without ride-sharing. The datasets are designed to represent spatial and temporal variations in input data for DARP.
The repository contains three datasets i.e. a spatial dataset, a temporal dataset and a growth dataset.

##Directories Description
**Spatial-DS** = A spatial dataset that has fixed service duration while the area of service varies from 5 to 60 square km.

**Temporal-DS**= A temporal dataset that has a fixed area of service while the service duration varies from 4 to 24 hours.

**Growth-DS**  = This dataset has fixed service duration and area of service while the number of requests (or number customers) varies from 50 to 1000. 

All the datasets have the following common characteristics,

(a)	The location of the depot is selected at the center of area of service.

(b)	Pick-up and drop-off points are randomly generated using uniform distribution.

## Files Description
  
### File Name
The names of the files contain four information, i.e. dataset type, Service Duration (SD), Service Area (SA) and the number of 
customers or number of requests (indicated by c, only for the Growth-DS). For example the file named 'Growth_SD12hrs_SA10km_c50'
means that the file belongs to growth dataset, has the service duration of 12 hours, service area of 10 square km and has 50 customers or requests. 
### File contents 
The first row of each file represents the coordinates of the depot.
The subsequent rows should be processed as

|ReqNo|	SrcPoint_x|	SrcPoint_y|	DstPoint_x|	DstPoint_y|	DRT |	MRT |	Pick-up/Drop-off time|Flag |
------|-----------|-----------|-----------|-----------|-----|-----|----------------------|-----|
ReqNo       =  The request or customer number.

SrcPoint_x= The x-coordinate of customer pick-up point.

SrcPoint_y= The y-coordinate of customer pick-up point.

DstPoint_x= The x-coordinate of customer drop-off point.

DstPoint_y= The y-coordinate of customer drop-off point.

DRT= Direct Ride Time. The time needed to transport the customer between Src and Dst point on the shortest path without any deviations. 

MRT= Maximum Ride Time (calculated by adding 60 minutes to the direct ride time of the customer).

Pick-up/Drop-up time= Pickup or drop-off time of the customer determined by the flag.

Flag=  A Boolean value that indicates if the time in previous column is pick-up (1) or drop-off (0) time.
