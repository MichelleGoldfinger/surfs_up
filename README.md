# surfs_up

## Overview of the analysis: Explain the purpose of this analysis.
My client would like more information about temperature trends before opening the surf shop. Specifically, he wants temperature data for the months of June and December in Oahu, in order to determine if the surf and ice cream shop business is sustainable year-round.

## Results: Provide a bulleted list with three major points from the two analysis deliverables. Use images as support where needed.
  -The mean temperature in Oahu in June is 75 degrees and the mean temperature for Dec is 71 degrees.
  -The minimum temperature in Oahu in June is 64 degrees and the the minimum temperature in Oahu in Dec is 56 degrees.
  -The maximum temperature in Oahu in June is 85 degrees and the maximum temperature in Oahu in Dec is 83 degrees.
  
<img width="259" alt="June Temps" src="https://user-images.githubusercontent.com/75905911/109366294-0e2e2c80-7861-11eb-8046-f0d0dea8c697.png">

<img width="227" alt="Dec Temps" src="https://user-images.githubusercontent.com/75905911/109366301-14240d80-7861-11eb-9d94-aa33de76bc3a.png">


## Summary: Provide a high-level summary of the results and two additional queries that you would perform to gather more weather data for June and December.

In Oahu, the average temperature in June is 75 degrees and in Dec the average is 71. In June the minimum temperate is 64 degrees and in December it is 56 degrees. The maximum temperature in June is 85 degrees and it is 83 degrees in December.

Two additional queries:

results = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date)==6).all()
print(results)

This query would give a list with precipitation amounts for June.

results = session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date)==12).all()
print(results)

This query would give a list with precipitation amounts for Dec.
