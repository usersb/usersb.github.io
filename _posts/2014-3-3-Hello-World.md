---
layout: post
title: DataScience Journey Begins...
---
----------------------------------------------------------------------------------------------------------------------------------------

I’m absolutely amazed at what this field of data science has achieved in terms of self driving cars, identifying human form, 
reading letters, numbers off of a picture and much more. The more I read about these amazing achievements the more I get 
interested in the field and makes me want to contribute.

I'm really grateful to my professor at New York University - Foster Provost, who first instilled the interest for data science
in me. I really enjoyed studying data mining and practical data science under his guidance. Unfortunately I didn't get a chance
to apply my data science skills on my job after graduation. I took a career break to look after my then new baby who's now an
adorable toddler. Instead of letting this break become a roadblock, I considered it a blessing in disguise to get back to 
honing my data science skills. I opted for a couple of MOOCs and thereafter completed Stanford's online Machine Learning course
taught by professor Andrew Ng. This course really amped up my interest in machine learning and I decided to pursue it full time
in order to accomplish some interesting projects by working through the entire data science project life cycle. 

Metis is a 12 week immersive datascience bootcamp which provided me the opportunity I was looking for. Metis's 60+ hours of 
pre-work was quite interesting to work on and helped bridge the gaps in my knowledge. I hope my Metis experience takes my data 
science pursuit up a notch.

**Metis Data Science Bootcamp**

My first week at Metis is done! I has been fast paced, demanding and a great experience so far. Although, for me it was a rough
start as my week started with cold, flu and conjunctivitis. So the bootcamp start was overwhelming for me to some extent. But 
as the week progressed it got much better and I started enjoying the bootcamp.

My cohort comprises of 21 students from varied backgrounds in terms of education, work experience and domains. Some
of the students are highly skilled in programming while the others have great statistics skills. The cohort is a good 
amalgamation of all the skils required to be a good data scientist and we hope to learn and benefit from each others strengths.  

The class is conducted by two friendly,helpful and highly knowledgable instructors. A typical day at the bootcamp consists of
pair programming in the morning followed by lecture till lunch. The session post lunch consists of another lecture for around 
two hours. After the lecture students work on challenges and/or projects.  

**Metis Week One - Project Benson**  

The first week at the bootcamp focused on lectures on pandas- a python package for data analysis as well as a quick overview of
matplotlib and seaborn - python plotting and data visualization libraries. Learning all these skills help us download data,
clean and perform exploratory data analysis and find interesting insights from the data. These learnings were applied towards
the first project at the bootcamp - Project Benson.  

Project Benson was a group project and we were a team of five members. For project Benson, we were required to provide 
consultation to a company - NyBER which was seeking aid for the New York city chapter of their transportation business.
NyBER needed help resolving the following concerns:  
1. Declining revenue (2016 Q2, Q3,Q4)  
2. Taxi wait times increased by 50%+  
3. Overall customer experience declined by 60%  
The data that Metis wanted us to explore for this project is the MTA Subway Turnstile data which is publicly available at 
[MTA Turnstile data](http://web.mta.info/developers/turnstile.html). The deliverable was to provide insights and recommendation to NyBER
at the end of the week as to how they can improve revenue and capture a major share of the local taxi market.  

Metis's idea behind the project was to get the students work in a team, getting to know each other in the process, experience
the advantages and challenges one can get working as a team.  
Practice working on presentations and presenting it to an audience of considerable size since data science is all about working 
and presenting or communicating the work.  

**Project Work**  

Following is a brief overview of the work our team performed on the project without delving into the technical details:  

1. Downloaded the MTA turnstile data from the source mentioned above for a period of four months within 2017. We decided to work 
on a subset of the data which targeted the weekday afternoon rush hour from 4pm to 8pm. The data provides a count of the entries
and exits at each of the turnstiles at each of the stations within NYC.  

2. Cleaned the data -  
   * Made sure all the column names were properly formatted.  
   * Identified and removed duplicates.  
   * Removed the data where the description was 'RECOVR-AUD' and only used the data with 'RECOVER' value for the description 
      column.  
   * After discovering that the turnstile counts were cumulative, we calculated the actual exits per time period.  
   
3. We added up the exits to calculate the total traffic per station for the afternoon rush hour period for a duration of four
months.  
4. At this point we were able to populate a map with commuter hotspots based on real-time analytics. By aggregating the traffic 
that occurs at a station Monday to Friday - 4pm to 8pm, our team was able to rank all the stations based on commuter traffic.
A map of this data is depicted in the figure below.  

![an image alt text]({{ site.baseurl }}/images/img_1.png "Fig. 1 A map illustrating station exits across a 4 PM - 8 PM weekday 
time period. Large bubble size indicates more station traffic.")

A bubble has been plotted for each station and the size of each bubble relates to the amount of traffic exiting the station. The
large bubbles on the map therefore belong to the busiest stations on the subway network. It is apparent from the map that the 
busiest stations are located in and around the manhattan area with smaller pockets of station traffic in other boroughs.  
The map also highlights a number of stations clustered outside of manhattan that have individually small traffic bubbles but quite
a large aggregate count. By assigning each station a count that is an aggregation of its own and its surrounding station counts,
we can identify overlooked commuter hotspots.  
 
We have given an example below about how the traffic metric of a station significantly increases when it takes in account the 
traffic at stations which are 10 minutes drive away.  
When this method of calculating a traffic metric is applied to all stations, it reveals that large commuter hotspots exist in 
areas that aren't typically considered. These are often comparable in size to some of the busiest stations in the most fiercely 
congested areas between taxi firms.  

As an example, we looked at the Barclay's center area in Brooklyn. There are number of 'low traffic' stations within a smaller 
proximity of each other. Figure 2 below illustrates all the stations within a ten minute driving time from the Barclay's center 
station (based on google maps time estimation).   

![an image alt text]({{ site.baseurl }}/images/img_2.png "Fig 2. There are a number of stations within close proximity of each
 other and examining station traffic by area warrants further analysis.")
 

Figure 3 below shows the aggregated exit data for stations clustered around the Barclay's center(in blue) is comparable to the 
numbers of commuter traffic seen in the busiest manhattan stations.  

![an image alt text]({{ site.baseurl }}/images/img_3.png "Fig 3. Aggregated exit data for stations clustered around the Barclays
Center (in blue) is comparable to the numbers of commuter traffic seen in the busiest Manhattan stations.")
  

**Conclusion**   

At present taxi drivers are left to themselves to decide where to roam for customers. They typically roam around know tourist
maps like the Time Square or the Empire State building. While these locations have very high commuter traffic, they also have
very high taxi density.  
Based on our analysis, we have identified key hotspots within many traditionally overlooked areas. We would like to recommend
NyBER a taxi dispatching system that sends drivers to the nearest calculated hotspot based off of their current location.  

In addition to the taxi dispatch platform, there are also additional data metrics we can take into account not depicted in this
solution that can increase NyBER's competitiveness. By scaling the aggregate count of each station by an aggregate 'isolation
factor', we can weigh station clusters that are around less public transportation.  
Most New Yorkers use the MTA to get around the city. It's typically at more isolated stations to call a cab than they think. By 
weighing  our traffic data by the isolation of a transportation cluster, we can further the effectiveness of NyBER's dispatch
system.  
 
------------------------------------------------------------------------------------------------------------------------------------