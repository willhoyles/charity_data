# charity_data
An analysis of data available from opencharities.org

## Distribution of charities across location and time
### Introduction
This project uses data from http://opencharities.org/ which pulls data from the Charity Commission into a usable API. I downloaded a database of roughly 370,000 registered charities, including many that were now closed, on 21 December 2020. I've used geographical plotting and other graphing techniques to look at the distribution of charities across the UK and at how the distribution across regions and sectors has changed from the 1960s to the 2010s.

### Brief conclusions
Unsurprisingly, there is a significant weighting of charities towards the South-East, and London in particular. The scale of that concentration and its acceleration since the 1990s was more significant than expected. Even outside of London charities are heavily focused around populous areas. The types of activity, sector and beneficiary of charities doesn't greatly vary by region.

The list of charities has been filtered to remove those charities that have since closed so it is perhaps not surprising that there are more charities that have been established recently in each each sector and location but it does imply that many charities have a shelf life. There are some notable outliers that are discussed below.

## Data dictionary:
### charity_clean.csv
This is the main spreadsheet downloaded from opencharities.org in December 2020. It contains roughly 250,000 records.
Columns | Not null | Definition | dtype
 --- | --- | --- | ---
 Unnamed: 0 |                    138020 | irrelevant | integer
 title       |                   138020 | name of the charity | string
 charity_number    |             138020 | Charity Commission charity number |integer
 activities        |             104722 | Description of the charity's activity | string
 contact_name      |              13855 | A named individual at the charity | string
 address            |            138020 | The full address of the charity | string
 website             |            75663 | URL of the charity's website | string
 telephone           |           136154 | A telephone number | string
 date_registered      |          138019 | The date the charity was added to the register - equivalent of when the charity was established | string
 date_removed         |               0 | The date the charity was removed from the register - Empty | n/a
 accounts_date        |           99963 | Date of the most recent accounts | string
 spending             |              91| Amount spent by the charity in the last accounts | integer
 income               |              91 | Amount of income the charity received in the last accounts | integer
 opencharities_url    |          138020 | URL of the charity's page on opencharity.org | string
 twitter_account_name |            9123 | the charity's Twitter username | string
 facebook_account_name|            6144 | the charity's Facebook username | string
 youtube_account_name  |           3345 | the charity's Facebook username | string
 feed_url              |           6151 | the URL of an RSS style newsfeed | string
 charity_classification_uids |   137584 | a series of three digit codes representing the activities of the charity - meaning of codes is in Charity_commission_codes.csv | string
 last_checked                |   138020 | the date the information was last updated from the Charity Commission website | string
 created_at                  |   138020 | the date the record was created in the opencharities.org website | string
 updated_at                  |   138020 | the date the information was last updated from the Charity Commission website (not sure how this is different to last_checked | string
 post_code                   |   138020 | The postcode of the charity extracted from the address record (my addition) | string
 longlat                      |  138020 | The longitude and latitude of the postcode (my addition) | string
 geometry                     |  138020 | A shapefile format point location of the longitude and latitude | string
