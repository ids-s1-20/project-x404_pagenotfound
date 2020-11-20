# Code Book for Data File - Volcanos 


## volcano.csv
Volcano data frame has the dimensions - dimensions 958 x 26
In the volcano data frame, each row represents one of the earths volcanos, containing information on a volcanos name, geographical location, the type of volcano it is and the rock type it consistent of.

- `volcano_number`: Volcano unique ID
- `volcano_name`: Volcano name
- `primary_volcano_type`: Volcano type (see wikipedia above for full details)
- `last_eruption_year` : Last year erupted
- `country`: Country
- `region`: Region
- `subregion`: Sub region
- `latitude`: Latitude
- `longitude`: Longitude
- `elevation`: Elevation
- `tectonic_settings`: Plate tectonic settings (subduction, intraplate, rift zone) + crust
- `evidence_category`: Type of evidence
- `major_rock_1`: Major rock type
- `major_rock_2`: Major rock type
- `major_rock_3`: Major rock type
- `major_rock_4`: Major rock type
- `major_rock_5`: Major rock type
- `minor_rock_1`: Minor rock type
- `minor_rock_2`: Minor rock type
- `minor_rock_3`: Minor rock type
- `minor_rock_4`: Minor rock type
- `minor_rock_5`: Minor rock type
- `population_within_5_km`:Total population within 5 km of volcano
- `population_within_10_km`: Total population within 10 km of volcano
- `population_within_30_km`: Total population within 30 km of volcano
- `population_within_100_km`:Total population within 100 km of volcano

## eruptions.csv
Erruptions data frame has the dimensions - dimensions 11,178 x 15
In the eruptions data frame each row represents a volcano eruption that has occurred, containing information on what volcano errupted, the type and scale of the erruption, as well as when it strted and finished.
- `volcano_number`: Volcano unique ID

- `volcano_name`: Volcano name
- `eruption_number`: 	Eruption number
- `eruption_category`: Type of eruption
- `area_of_activity`: Area of activity
- `vei`: Volcano Explosivity Index (0-8) see wikipedia above
- `start_year`: Start year
- `start_month`: Start month
- `start_day`: Start day
- `evidence_method_dating`: Evidence for dating volcano eruption
- `end_year`: End year
- `end_month`: 	End Month
- `end_day`: End day
- `latitude`: Latitude
- `longitude`: Longitude

## events.csv
Events data frame has the dimensions - 41,322 x 10
In the events data frame each row represents an event which has occured. An event in the context of this dataframe is an erruption of a volcano. Each row contains information on what volcano and erruption the event consists of, as well as when the event occured.
- `volcano_number`: Volcano unique ID

- `volcano_name`: Volcano name
- `eruption_number`: 	Eruption number
- `eruption_start_year`: Eruption start year
- `event_number`: Event number
- `event_type`: 	Event type
- `event_remarks`: Event remarks
- `event_date_year`: Event year
- `event_date_month`: 	Event month
- `event_date_day`:	Event day
