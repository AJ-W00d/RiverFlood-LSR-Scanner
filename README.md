README: River Flooding Impacts Analysis

Overview

This Jupyter Notebook, River_Flooding_Impacts.ipynb, contains a comprehensive analysis of local storm reports (LSRs) related to flooding. The analysis focuses on correlating LSR data with nearby USGS river gage observations and forecasts to provide insights into flood events over the past 20 years.

Data Sources

Local Storm Reports (LSR): Obtained from the Iowa State University Iowa Environmental Mesonet (IEM LSR Data)

USGS River Gage Data: Pulled from the National Water Prediction Service (NWPS).

Objective

The primary goal of this notebook is to analyze LSRs labeled as "Flood" that occurred within a 5-mile radius of an RFC Observation/Forecast point. The notebook then captures and presents the stage and status of the nearest USGS river gage at the time of the flood event.

Notebook Features

Load and preprocess LSR and USGS gage data.

Perform spatial analysis to identify the nearest gage for each LSR.

Retrieve and analyze the stage and status of the nearest gage at the LSR's valid time.

Generate suggested comments for Flood Impact Assessments.

Data Fields Description

Local Storm Report Data

fid: Feature ID (ESRI requirement)

LSR_Date/Time: Date and time of the LSR (e.g., 202205051637.0 for May 5, 2022, 16:37)

Lat, Lon: Latitude and longitude (decimal degrees) of the LSR

WFO: Weather Forecast Office issuing the report

Event_Type: Always labeled as "FLOOD"

City, County, State: Location information

Source: Source of the report

Remark: Description of the flooding impact

Generated Data

Nearest_Gage: NWS LID of the nearest USGS gage

Gage_Location: Nearest USGS gage location

Gage_Waterbody: Name of the waterbody where the gage is located

Gage_State: State abbreviation of the gage location

Action_Threshold, Minor_Threshold, Moderate_Threshold, Major_Threshold: Gage flood thresholds (in feet)

Gage_URL: URL for detailed information on the gage

LSR_to_Gage_Distance_(miles): Distance between the LSR and the nearest gage

USGS_ID: USGS gage identification number

Event_Stage_(ft): Gage stage (in feet) at the LSR time

Event_Status: Status of the nearest gage at the LSR time

Gage_Observation_Date/Time: Date and time of the nearest gage observation

LSR_Link: URL link to the specific LSR

Suggested_Comment: Pre-generated comment for use in Flood Impact Assessments

Event_Status_Code: Gage status code indicating flood severity:

0: No Flood (not included)

1: Action Stage (not included)

2: Minor Flood

3: Moderate Flood

4: Major Flood

Usage

Open the notebook using JupyterLab or Jupyter Notebook.

Ensure all necessary dependencies are installed using pip install -r requirements.txt.

Execute each cell sequentially to perform data analysis.

Review results and suggested comments in the output cells.

Additional Notes

This analysis is useful for flood impact reviews and assessments.

Ensure proper data access permissions for the data sources mentioned.

Customize distance thresholds or data filters as needed.

License

This project is provided under the MIT License.
