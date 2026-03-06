# Data Reporting Story Pitch 

# Hundreds of unaccompanied children go to a rural Washington County, and its classrooms

A rural Washington county has one of the state’s highest numbers of unaccompanied migrant children, trailing only Seattle-area counties. Seventy percent of these children are not going to their parents.

Mason County received 412 unaccompanied children from January 2015 through May 2023, according to data from the U.S. Department of Health and Human Services. This is more than triple the county average in Washington state. Of these children, 60% were placed with non-parent sponsors. 

Since 2015, there has been a similar number of migrant children arriving. As they arrive and adapt to living in Mason County, school can be a place of support and structure. Do the local schools in Mason County have programs to help this population of students settle? 

This reporting will build on The New York Times' investigation “Where Migrant Children Are Living, and Often Working, in the U.S.,” which marked Mason County as the hotspot of Washington for non-parent sponsor placements. Exploring how or if school districts address this population of children can show how local policies and organizations have adapted to account for the number of migrant children coming to Mason County. 

# Limitations

The HHS data that I have tracks the initial county where each child is released, but it does not show whether the child remains there for long. Therefore, if these children are not enrolling in school in this county, this could impact the number of programs that are being created or managed to address this population. 

# Methods 

This analysis uses federal data from the U.S. Department of Health and Human Services, which was made public by The New York Times (https://github.com/nytimes/hhs-child-migrant-data). The dataset spans from January 2015 to May 2023. Each row represents an unaccompanied child released to a sponsor, with fields for the sponsor's zip code and category. I filtered the data for zip codes in Mason County and then used it to produce counts for sponsor type and totals over time.

To align sponsors' zipcodes with counties, I used the zipcodeR package to map each zipcode to its county FIPS, then joined the migrant child data to the appropriate counties throughout Washington. I merged these results with the 2023 American Community Survey county population estimates to create the choropleth map, which shows rates of children going to non-parent sponsors by 100,000.

I produced the visuals in my R Markdown file, titled mason-migrant-children-pitch.Rmd. These include:
- Sponsor category bar chart: Determined using Mason County releases by sponsor category data. 
- Change over time line chart: Quarterly totals for Mason County, with the share going to non-parent sponsor highlighted. 
- Choropleth map: Joined county totals to the Washington shape file to visualize the share of non-parent placements across the state by county. 
