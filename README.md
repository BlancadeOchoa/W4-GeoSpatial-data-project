
# W4-GeoSpatial-data-project

We recently created a new company in the **gaming industry**, so, therefore, this project consisted of finding the **best place to locate our office** in order for our company to grow. 
We had some initial requirements;

- Designers like to go to design talks and share knowledge. There must be some nearby companies that also do design.

- 30% of the company have at least 1 child.

- Developers like to be near successful tech startups that have raised at least 1 Million dollars.

- Executives like Starbucks A LOT. Ensure there's a Starbucks not too far.

- Account managers need to travel a lot

- All people in the company have between 25 and 40 years, give them someplace to go partying.

- The CEO is Vegan

- If you want to make the maintenance guy happy, a basketball stadium must be around 10 Km.

- The office dog "Pepe" needs a hairdresser every month. Ensure there's one not too far away.


![Getting Started](Pictures/workspace.jpg)



# Steps followed:

I read the requirements and select the most crucial ones and assign them punctuation from 1 to 5 in order of what I considered where more important for the company.
These punctuations gave the order of filtration I followed;
1. Being close to a design company
1. Being close to a tech company with more than 1M dollars raised
2. Being close to an airport
3. Near to nightlife places
4. Proximity to a nursery school
5. Proximity to vegan restaurants
6. Proximity to a basketball stadium

## FILTER 1 and 2: Design and Tech

I use mongo db to analyze the data set, by classifying the companies by their **category code**. I chose to select all the companies that followed this condition and ended up with four of them, located in 4 different cities; **Berlin, San Francisco, Ellensburg and Collingwood**.

To further this analysis I took these four cities and checked wich one had more **tech companies in their proximity** by using the function near and a max distance. From this analysis, **San Francisco** is by far the best city because it has the most companies that followed these two conditions.

## FILTER 3: Airport

After knowing I am working with one city I reduce a lot the number of companies by making a near query to the airport to **only 5**.

## FILTER 4: Nightlife

At this point of the filtering, I start using the **foursquare API**, which consists of using coordinates and a query to find venues in their proximity.
Firstly I start with **venues that belong to nightlife**, in a radius of 100m from the office and reduce the number of companies **from 5 to just 3**.

## FILTER 5: Nursery school

Following with foursquare I use a new query, being close to a **nursery school**, considering that this will be very important due to the age range of the employees.
I consider a **radius of 250m** and reduce the companies **from 3 to 2**.

## FILTER 6 and 7: Vegan restaurant and Basketball stadium

At last, I keep using the foursquare API to perform the last two filters. The queries where Vegan Restaurants where both companies passed the filter because I choose as a radius 500 m and decided this was enough.
The last query used was a basketball stadium, and this finished de search by  only remaining the first company: 

'Gen-Y Media',
  'offices': {'country_code': 'USA',
   'latitude': 37.598478,
   'longitude': -122.376572}}

## Last steps

Once the search has ended, using **folium** I represent in a map the final location and **create a marker** for each query I choose to filter with.

# Challenges faced

![Getting Started](Pictures/challenges.jpg)

The challenges I faced while doing this project where mainly timewise, I felt like I had very little time for all the functions and queries I wanted to preform. 
More specifically with one of the lasts steps, I wasn't able to create a for loop to reduce the code in order not to repeat it so much. And I also would have liked to create more maps and analyze the results more into detail with folium but didn't have enough time.


