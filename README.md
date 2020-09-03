# Waterhackweek 2020: Fire and Water
### How do wildfires impact lakes?

* Slack channel: [#fire-and-water](https://waterhackweek2020.slack.com/messages/C019MP15H70) 

* Google drive: https://drive.google.com/drive/folders/1he4AevUwBnyOu1mv9Gttn7MJImSd7cvc

---

### Collaborators:
* Bethel Steele & Brent Wilder (Project Leads)
* Steven Pestana (Data Science Lead)

* Science team: Kim Vincent, Porranee Thanapakpawin, Ning Ren, Vitaliy Ye., Dani Hunt, Megan Duffy

---

### The problem:

Wildfire regimes are shifting in western North America as global temperatures rise and combine with the effects of historial fire suppression and increased bark beetle infestations. The wildfire season is growing longer and more intense, with fire burning hotter and covering more land. The effects of local catastrophic wildfire on water quality and ecological changes in lakes, however, are poorly understood. In this project, we pursue the following questions using remote sensing data:

* What is the impact on lake surface temperature after fire?
* What are the timescales water quality shifts after a fire?

With an initial focus on a single lake in northeastern California, our goal is to develop an analysis framework easily reporducible and applicable to other aquatic systems affected by fire.

### The case study: Clear Lake Reservoir, CA

![Tucker fire reaches Clear Lake in 2019](https://github.com/MeganEDuffy/whw2020_firewater/blob/master/tucker-fire-clear.jpeg)
*Tucker fire reaches the shores of Clear Lake Reservoir, July 2019, photo Brian Gailey- Klamath Falls News*

The Upper Lost River/Clear Lake Reservoir watershed drains the north-central portion of the Modoc Plateau to the Clear Lake Reservoir, which feeds the Lost River, a tributary of the Klamath River. After the dam at Clear Lake (constructed in 1910 and replaced in 2002) the Lost River flows northwest into Oregon, traversing about 100 miles before returning to California and ending in a closed drainage basin at Tule Lake, including reclaimed wetlands in the Tule Lake National Wildlife Refuge, a key staging area for migrating waterfowl in North America. Clear Lake Reservoir is part of Modoc National Forest and protected as Clear Lake National Wildlife Refuge. The reservoir's water supplies irrigation in the eastern portion of the Klamath Basin. 

Clear Lake Reservoir has experienced large wildfire events in the recent past, including the Tucker Fire in July 2019 (14,150 acres) which burned to the lake's rim. Additional information:

- 41.860 °N 121.146 °W; elevation: 1367 m (4485 ft)

- Lake surface area: 104 7 km<sup>2</sup> (25760 acres)

- Ave. depth at max. capacity: 6 m (20 ft)

- Water volume: 0.650 km<sup>3</sup> (527000 acre⋅ft)

### Land and water acknowledgement: 

The Clear Lake Reservoir is a small part of the ancestral homelands of the Modoc people, who have stewarded these lands and waters from time immemorial to today. Ignoring earlier proposals of the Modoc, Klamath, and Yahooskin Band of Snake tribes, the United States forcibly negotiated a Treaty of Council Grove in 1864 (also called the Klamath Tribes Treaty, ratified in 1870) that endangered tribal land and water rights and established the Klamath Reservation north of traditional Modoc land. The cultural, spiritual, and economic health of the Klamath peoples is inseperable from the health of their lands and waters.

---

### Specific goals:
* Learn to access and manipulate remote sensing data and time series meteorological data using python
* Build a data aquisition and analysis framework applicable to other sites

---

### Broader impacts:

* Answering questions about lake surface temperature disturbances leads to implications for ecosystem impacts 
* Potential for interpolation to lakes too small for remote sensing surface temperature determination

---

### Data sources:

* Monitoring Trends in Burn Severity (MTBS) - [MTBS Interactive Viewer](https://www.mtbs.gov/viewer/index.html)
* ECOSTRESS geotiff files and use to visualize spatial distribution surrounding fire event
* MODIS time series 10 year recond from [Google Earth Engine](https://earthengine.google.com/)
* Snow Telemetry - [SNOTEL](https://www.nrcs.usda.gov/wps/portal/wcc/home/quicklinks/imap#version=125&elements=&networks=!&states=!&counties=!&hucs=&minElevation=&maxElevation=&elementSelectType=all&activeOnly=true&activeForecastPointsOnly=false&hucLabels=false&hucIdLabels=false&hucParameterLabels=true&stationLabels=&overlays=&hucOverlays=2&basinOpacity=75&basinNoDataOpacity=25&basemapOpacity=100&maskOpacity=0&mode=data&openSections=dataElement,parameter,date,basin,options,elements,location,networks&controlsOpen=true&popup=&popupMulti=&base=esriNgwm&displayType=station&basinType=6&dataElement=WTEQ&depth=-8&parameter=PCTMED&frequency=DAILY&duration=I&customDuration=&dayPart=E&year=2020&month=8&day=31&monthPart=E&forecastPubMonth=6&forecastPubDay=1&forecastExceedance=50&seqColor=1&divColor=7&scaleType=D&scaleMin=&scaleMax=&referencePeriodType=POR&referenceBegin=1981&referenceEnd=2010&minimumYears=20&hucAssociations=true&lat=42.1008&lon=-121.0913&zoom=10.0) 
* [DayMet](https://daymet.ornl.gov/) gridded estimates of daily weather parameters
* Possible: monthly evapotranspiration data from SSEBop model based on MODIS
* Possible future integration of buoy data and/or low-resolution in situ profile temperature, chlorophyll-a, nutrients, sediment load, or geophysical properties

#### Project data repositories and resources

* [Data readme](https://github.com/waterhackweek/whw2020_firewater/tree/master/data)
* [Google drive folder](https://drive.google.com/drive/folders/1he4AevUwBnyOu1mv9Gttn7MJImSd7cvc)
* Hydroshare resource

---

### Existing methods/tools and prior work:

* [Grabbing SNOTEL data](https://github.com/renjianning/whw2020_firewater/tree/master/Scripts) (from Ning)
* [Creating a hydroshare resource](https://www.hydroshare.org/resource/7015162a158648ba95ff547a6eb753ba/)


---

### Python Packages Used:

* numpy
* pandas
* [xarray](http://xarray.pydata.org/en/stable/)
* [geehydro](https://github.com/giswqs/geehydro)
* matplotlib
* [folium](https://pypi.org/project/folium/)

---

### Background Reading:

* UC Davis science brief - [Rim Fire impacts on Sierra Lakes](https://tahoe.ucdavis.edu/rim-fire)
* Oleksy, I.A, Beck, W.S., et al. "The role of warm, dry summers and variation in snowpack on phytoplankton dynamics in mountain lakes" Ecology (2020) [DOI:10.1002/ecy.3132](https://esajournals.onlinelibrary.wiley.com/doi/abs/10.1002/ecy.3132)
* Silins, U., Bladon, K.D., et al., "Five-year legacy of wildfire and salvage logging impacts on nutrient runoff and aquatic plant, invertebrate, and fish productivity" Ecohydrology (2014) 7(6) [DOI: 10.1002/eco.1474](https://onlinelibrary-wiley-com.offcampus.lib.washington.edu/doi/full/10.1002/eco.1474)
* Kelly, E.N., Schindler, D.W., et al., "Forest fire increases mercury accumulationby fishes via food web restructuringand increased mercury inputs" PNAS (2006) 103(51) [DOI:10.1073/pnas.0609798104](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1693476/)

---

### Getting started with the *firewaterenv* conda environment

Create the environment:

`conda env create -f environment.yml`

Activate the environment:

`conda activate firewaterenv`

If using the Google Earth Engine API, authenticate your account to access it:

`earthengine authenticate`

Then:
* Shift+RightClick > Copy the URL
* Go to the URL and then log in to your GEE account when prompted
* Copy the authentication token from the website
* Paste the authentication token in the terminal then press Enter


[More information about working with conda environments](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#sharing-an-environment)

[More information about the GEE API](https://developers.google.com/earth-engine/guides/python_install-conda)