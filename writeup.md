![Title][title]

# So You Want To Be a Landlord...
A look through the Airbnb public database to see what hosts are up to

## Introduction

On paper, property rental is a great business.  A successful property will generate revenue as it increases in equity.  But like any investment, it's also very easy to lose money.  Real estate is expensive.  Because even the very minimum investment is large enough to require financing, a successful rental property will need to show a profit very soon.

There are other intangibles.  Even though it's considered a passive income, it can be a lot of work.

- The Airbnb data sets available on Kaggle are examined.
- The data comes from 2 cities, Boston and Seattle, for a combined total of about 15,000 listings.
- A business really needs to know its _customers_, but this database is mainly about the _rental properties_. Still, we can work with the data available.

Data is available to address the other questions, or at least infer answers. We can use the rationale that real estate is a commodity, and the majority of rental businesses operate profitably. So, "we can't go too far wrong" by copying the competition. This is not an optimal business model for the long term. But for an initial investment in an unfamiliar market, it will answer the questions better than random guessing.

Have turned our attention to the competition, we want to follow the business model of successful hosts. Not every property is suitable for rental, and we don't want to emulate the failures. We can weed some of them out by looking at 'established' rental properties, as evidenced by how long they've been getting reviews.

A histogram of the age of first_reviews does not provide a whole lot of insight, other than the business is seasonal. Using intuition and a little domain knowledge, we can say somewhat arbitrarily that if the first_review is less than 12 months old, the property is still in its 'trial period'. This choice will also allow us to safely use the number_of_reviews_ltm field. (LTM stands for 'last twelve months'.)



### What duration of rental is most common?

Even in its simplified form, this question can't be answered directly. But we know the values are bounded by minimum and maximum nights, so this value is bounded. Of course, in most cases there is no upper bound, so really we can only look at the minimum.

*** GRAPHIC ***

The curve is (almost) bimodal. The vast majority of rooms have a minimum of 1 week or less, (hence the 'BnB' in 'AirBnB',) with a small lump at 30 days.

The most common minimum is 2 nights. This might seem a little surprising at first, but in a well-established industry such as this, there are generally reasons for things.



### Which locations are most popular?

*** GRAPHIC ***

There are many landmarks we could choose, but proximity to 'downtown' (as defined by Bing maps) is probably good enough. A more detailed investigation might include proximity to other attractions, such as universities or tourist attractions.

Most established Airbnb rentals are within 5 miles of the city center. Boston is more compact, so it's not surprising that the rental units are clustered more tightly.

Most rentals are near the city center, so naturally we expect to see more reviews towards downtown. But, it seems that the units farther away generate plenty of reviews as well, including many of the highest performing properties.



### What type of accomodation is most common?

*** GRAPHIC ***

The mean rental size is 742 sq ft, with the most common size being around 500 sq ft.

The most common rental accomodates 3 people. Yet, the most common rental also has a single bedroom with a single bed.

The most common rental has a single bathroom, which would be logical for a 500 sq ft, 1-bedroom apartment.



### Which locations/types of properties bring in the largest rent?

*** GRAPHIC ***

Prices in Boston and Seattle are not an apples-to-apples comparison, so these are graphed separately. Boston is more expensive than Seattle, which is to be expected. Real estate prices in general have a positive skew, and these plots are no exception. The median price is more commonly used for this reason.

Boston skews further to the right than Seattle, and this difference becomes more pronounced as the duration of the stay increases. The monthly rate for Boston has a strong positive skew. This bears further investigation. For example, there could be local taxes or ordinances driving this.

*** GRAPHIC ***

The price has a generally a positive correlation between square footage, number people acommodated, and bedrooms. It stands to reason that a larger property will cost more. However, beds and bathrooms reach a peak value and then actually drop.

*** GRAPHIC ***

A larger property will only bring in more money if you're able to rent it out. We don't have rental histories, but we can roughly approximate it using the number of reviews in the last year. Although a little abstract, this set of graphs shows what customers are actually renting.

Generally speaking, smaller properties with fewer bedrooms and bathrooms are more popular. A studio apartments with a single full bathroom is the most popular.

The number of occupants and number of beds are pretty flat graphs, with the most popular having 3 beds.

*** GRAPHIC ***

Another significant finding is that the number of reviews in the last year is roughly a power distribution. Most properties receive few reviews, but a few properties receive many. This was not one of the original questions, I just happened to notice it when going over the data.

## Conclusion

TODO


### So do you REALLY you want to become a landlord?

To see more about this analysis, see the link to my Github available here.


[title]: https://www.aceshowbiz.com/images/still/project-x-image10.jpg