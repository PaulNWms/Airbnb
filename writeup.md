![Title][title]

# So You Want To Rent Out That Spare Room...
A look through the Airbnb public database to see what hosts are up to

## Introduction

On paper, property rental is a great business.  A successful property will generate revenue as it grows in equity.  But like any investment, it's also easy to lose money.  Real estate is expensive and generally requires financing.  A successful rental property will need to show a profit very soon.  

Therefore, choosing the right rental property is critical.  This article explores the characteristics of a successful Airbnb property.  The Airbnb data sets available on Kaggle are used as a data source.  The data comes from 2 cities, Boston and Seattle, for a combined total of about 15,000 listings.

A business really needs to know its _customers_, but this database is mainly about the _rental properties_. Still, we can work with the data available.  We also want to follow the business model of successful hosts.

Not every property is suitable for rental, and we don't want to emulate the failures.  Property rental is somewhat of a commodity industry, without a whole lot of room for innovation.  It's actually a valid business plan to keep an eye on the successful hosts and copy what works.  "You can observe a lot by just watching."

Of course, there are many concerns beyond choosing the right property.  Even though it's considered a passive income, renting out rooms can be a lot of work, requires some domain knowledge, and carries liability.  In the hotel business, the property manager is on-call whenever guests are on-site - which is hopefully most of the time.  Of course there is the daily task of cleaning the room and/or turning it for the next guests.  The operation of an Airbnb rental, and all that it entails, is beyond the scope of this article.

It is very important to pick the right property.  The rental history is not available in this database, but given the sample size, we can get a rough sense of the relative popularity by looking at the number of reviews per year.  A few "star" properties receive a lot of reviews, whereas most do not get very many at all.

![Reviews_Last_Year]

### What duration of rental is most common?

This question can't be answered directly. But we know the values are bounded by minimum and maximum nights. Of course, in most cases there is no upper bound, so really we can only look at the minimum.

![Minimum_Nights]

The curve is (almost) bimodal. The vast majority of rooms have a minimum of 1 week or less, (hence the 'BnB' in 'Airbnb',) with a small lump at 30 days.

The most common minimum is 2 nights. This might seem a little surprising at first, but in a well-established industry such as this, there are generally reasons for things.

### Which locations are most popular?

There are many landmarks we could choose, but proximity to 'downtown' (as defined by Bing maps) is probably good enough. A more detailed investigation might include proximity to other attractions, such as universities or tourist attractions.

![Distance_From_City_Center]

Most established Airbnb rentals are within 5 miles of the city center. Boston is more compact than Seattle, so it's not surprising that the rental units are clustered more tightly.

But real estate is complicated, and there are confounding factors.  Just because hosts tend to own properties downtown does not mean those are the most popular.

![Reviews_vs_Distance_From_City_Center]

Most rentals are near the city center, so naturally we expect to see more reviews towards downtown. But, it seems that the units farther away generate plenty of reviews as well, including many of the highest performing properties.

### What type of accomodation is most common?

![Size_Accomodation_Amenities]

The mean rental size is 742 sq ft, with the most common size being around 500 sq ft.

The most common rental accomodates 3 people. Yet, the most common rental also has a single bedroom with a single bed.

The most common rental has a single bathroom, which would be logical for a 500 sq ft, 1-bedroom apartment.



### Which properties bring in the most money?

![Price]

Prices in Boston and Seattle are not an apples-to-apples comparison, so these are graphed separately. Boston is more expensive than Seattle, which is to be expected. Real estate prices in general have a positive skew, and these plots are no exception. The median price is more commonly used for this reason.

Boston skews further to the right than Seattle, and this difference becomes more pronounced as the duration of the stay increases. The monthly rate for Boston has a strong positive skew. This bears further investigation. For example, there could be local taxes or ordinances driving this.

![Price_vs_Size_Amenities]

The price has a generally a positive correlation between square footage, number people acommodated, and bedrooms.  It stands to reason that a larger property will cost more.  However, beds and bathrooms reach a peak value and then level off, or actually drop.

![Reviews_vs_Size_Amenities]

A larger property will only bring in more money if you're able to rent it out. We don't have rental histories, but we can roughly approximate it using the number of reviews in the last year. Although a little abstract, this set of graphs shows what customers are actually renting.

Generally speaking, smaller properties with fewer bedrooms and bathrooms are more popular. A studio apartments with a single bathroom is the most popular.

The number of occupants and number of beds are pretty flat graphs, with the most popular having 3 beds.

## Conclusion

In this article, we explored property data from the Airbnb data sets available on Kaggle.  We observed that select properties are much more popular than most, using number of reviews as a rough indicator of popularity.  We looked at duration of rental, and found that a 2 night minimum was most common.  We found that most units are located near downtown, but also that those aren't necessarily the most popular with customers.  We found the most popular rental is a studio.

### So do you REALLY you want to rent out that spare room?

To see more about this analysis, see the link to my Github available here.


[title]: https://www.aceshowbiz.com/images/still/project-x-image10.jpg
[Reviews_Last_Year]: Reviews_Last_Year.png
[Minimum_Nights]: Minimum_Nights.png
[Distance_From_City_Center]: Distance_From_City_Center.png
[Reviews_vs_Distance_From_City_Center]: Reviews_vs_Distance_From_City_Center.png
[Size_Accomodation_Amenities]: Size_Accomodation_Amenities.png
[Price]: Price.png
[Price_vs_Size_Amenities]: Price_vs_Size_Amenities.png
[Reviews_vs_Size_Amenities]: Reviews_vs_Size_Amenities.png