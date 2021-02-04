# charity_data
An analysis of data available from opencharity.org

## Distribution of charities across location and time
### Introduction
This project uses data from http://opencharities.org/ which pulls data from the Charity Commission into a usable API. I downloaded a database of roughly 370,000 registered charities, including many that were now closed, on 21 December 2020. I've used geographical plotting and other graphing techniques to look at the distribution of charities across the UK and at how the distribution across regions and sectors has changed from the 1960s to the 2010s.

### Brief conclusions
Unsurprisingly, there is a significant weighting of charities towards the South-East, and London in particular. The scale of that concentration and its acceleration since the 1990s was more significant than expected. Even outside of London charities are heavily focused around populous areas. The types of activity, sector and beneficiary of charities doesn't greatly vary by region.

The list of charities has been filtered to remove those charities that have since closed so it is perhaps not surprising that there are more charities that have been established recently in each each sector and location but it does imply that many charities have a shelf life. There are some notable outliers that are discussed below.

## Data dictionary:
### charity_clean.csv
This is the main spreadsheet downloaded from opencharity.org in December 2020. It contains roughly 250,000 records.
Columns | Not null | Definition | dtype
 --- | --- | --- | ---
 Unnamed: 0 |                    138020 | irrelevant | integer
 title       |                   138020 | name of the charity | string
 charity_number    |             138020 | Charity Commission charity number |integer
 activities        |             104722 | Description of the charity's activity | string
 contact_name      |              13855 | 
 address            |            138020 |
 website             |            75663 |
 telephone           |           136154 |
 date_registered      |          138019 |
 date_removed         |               0 |
 accounts_date        |           99963 |
 spending             |              91|
 income               |              91 |
 opencharities_url    |          138020 |
 twitter_account_name |            9123 |
 facebook_account_name|            6144 |
 youtube_account_name  |           3345 |
 feed_url              |           6151 |
 charity_classification_uids |   137584 |
 last_checked                |   138020 |
 created_at                  |   138020 |
 updated_at                  |   138020 |
 post_code                   |   138020 |
 longlat                      |  138020 |
 geometry                     |  138020 |
