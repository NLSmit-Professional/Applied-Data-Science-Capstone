# Applied-Data-Science-Capstone

## Complete the Data Collection API Lab

using `https://api.spacexdata.com/v4/` as base 
make API calls (with requests libabry) to collect data from previous luanches such as payload, date and booster version
with some minor data wrangling
see dataset_part_1.csv


## Complete the Data Collection with Web Scraping Lab

using `https://en.wikipedia.org/wiki/List_of_Falcon_9_and_Falcon_Heavy_launches` 
perform webscraping (with BeatifulSoup library) to collect data from various tables 
see spacex_web_scraped.csv


## Data Wrangling
import data from csv directly using pandas library
see dataset_part_2.csv


## Complete the EDA with SQL
usinhg sqlite

```python
%load_ext sql

%sql sqlite:///:memory: # in-memory
#OR 
%sql sqlite:///data.db # file-based

df = pd.read_csv("---.csv")
# use the default connection from %sql (it's available as a global after connecting) 
## ELSE `con = sqlite3.connect(':memory:')` 
### BUT %sql handles this
df.to_sql("SQLdata", con, if_exists='replace', index=False,method="multi")

%%sql # OR %sql
CREATE TABLE example as SELECT * FROM SQLdata # duplicate data into new table
```


## EDA with Visualization Lab
