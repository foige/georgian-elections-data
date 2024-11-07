# 2024 Georgian Parliamentary Election (Round 1)

## Data

# cec_scrape_proportional_all.csv

Dataset contains the results of the 2024 Georgian Parliamentary Election for the proportional part of the election. 
The data was scraped from the Central Election Commission of Georgia's website (https://results.cec.gov.ge). 

All precincts, including electronic and traditional, are included in the dataset.

Columns `participated` and `invalid_ballots` are extracted using OCR of the protocols and may contain errors.

The dataset contains the following columns:

| Column Name                                                    | Description                                                                             |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| `lat`                                                          | Latitude coordinate of the precinct.                                                    |
| `lng`                                                          | Longitude coordinate of the precinct.                                                   |
| `info`                                                         | Additional information about the location or event.                                     |
| `name`                                                         | Name of the precinct.                                                                   |
| `year`                                                         | The year of the election.                                                               |
| `map_name`                                                     | Name used on the map display for the election.                                          |
| `address_1`                                                    | First line of the address associated with the precinct.                                 |
| `address_2`                                                    | Second line of the address, if applicable.                                              |
| `address_3`                                                    | Third line of the address, if applicable.                                               |
| `address_4`                                                    | Fourth line of the address, if applicable.                                              |
| `cancelled`                                                    | Indicates whether the election was cancelled (`True`/`False`).                          |
| `protocols`                                                    | URL to the protocols.                                                                   |
| `district_id`                                                  | Unique identifier for the district associated with the precinct.                        |
| `division_id`                                                  | Unique identifier for the precinct.                                                     |
| `internal_id`                                                  | Internal identifier for the election used for referencing within the dataset or system. |
| `archive_name`                                                 | Name of the archive or historical record associated with this entry.                    |
| `district_name`                                                | The name of the district where the event or election took place.                        |
| `election_type`                                                | Type of election (e.g., national, regional, etc.).                                      |
| `internal_name`                                                | Internal name or alias for the event used within the dataset.                           |
| `abroad_district_id`                                           | District identifier for precincts located abroad.                                       |
| `election_numeric_id`                                          | Numeric identifier for the specific election.                                           |
| `total_registered_voters`                                      | Total number of registered voters in this district or location.                         |
| `total_registered_voters_men`                                  | Total number of registered male voters in this district or location.                    |
| `total_registered_voters_women`                                | Total number of registered female voters in this district or location.                  |
| `participated`                                                 | Number of voters who participated in the election (OCR)                                 |
| `participated_confidence`                                      | Confidence level or reliability rating for the `participated` data.                     |
| `invalid_ballots`                                              | Total number of invalid ballots in the election (OCR).                                  |
| `invalid_ballots_confidence`                                   | Confidence level or reliability rating for the `invalid_ballots` data.                  |
| `total_votes`                                                  | Total valid votes cast in the election.                                                 |
| `CAND_3_საქართველოს ერთობისა და განვითარების პარტია`           | Votes received by candidate 3 (Party for Unity and Development of Georgia).             |
| `CAND_4_კოალიცია ცვლილებისთვის გვარამია მელია გირჩი დროა`      | Votes received by candidate 4 (Coalition for Change).                                   |
| `CAND_5_ერთიანობა-ნაციონალური მოძრაობა`                        | Votes received by candidate 5 (United National Movement).                               |
| `CAND_6_ევროპელი დემოკრატები`                                  | Votes received by candidate 6 (European Democrats).                                     |
| `CAND_8_საქართველოს პატრიოტთა ალიანსი`                         | Votes received by candidate 8 (Alliance of Patriots of Georgia).                        |
| `CAND_9_ძლიერი საქართველო-ლელო, ხალხისთვის, თავისუფლებისთვის!` | Votes received by candidate 9 (Strong Georgia–Lelo for People, for Freedom).            |
| `CAND_10_საქართველოს ლეიბორისტული პარტია`                      | Votes received by candidate 10 (Labour Party of Georgia).                               |
| `CAND_12_ჩვენი გაერთიანებული საქართველო`                       | Votes received by candidate 12 (Our United Georgia).                                    |
| `CAND_16_შეცვალე საქართველო`                                   | Votes received by candidate 16 (Change Georgia).                                        |
| `CAND_17_საქართველო`                                           | Votes received by candidate 17 (Georgia).                                               |
| `CAND_20_თავისუფალი საქართველო`                                | Votes received by candidate 20 (Free Georgia).                                          |
| `CAND_21_ტრიბუნა`                                              | Votes received by candidate 21 (Tribune).                                               |
| `CAND_23_ჩვენ`                                                 | Votes received by candidate 23 (We).                                                    |
| `CAND_25_გახარია საქართველოსთვის`                              | Votes received by candidate 25 (For Georgia by Gakharia).                               |
| `CAND_26_მემარცხენე ალიანსი`                                   | Votes received by candidate 26 (Left Alliance).                                         |
| `CAND_27_ქართველ ერთობა`                                       | Votes received by candidate 27 (Georgian Unity).                                        |
| `CAND_36_გირჩი`                                                | Votes received by candidate 36 (Girchi).                                                |
| `CAND_41_ქართული ოცნება`                                       | Votes received by candidate 41 (Georgian Dream).                                        |
| `CAND_999_Other`                                               | Votes received by other candidates not listed in specific columns.                      |

# cec_scrape_proportional_electronic.csv

Only electronic precincts are included in the dataset.

# cec_scrape_proportional_electronic_simple.csv

Simplified version of the electronic precinct dataset.

# cec_scrape_proportional_electronic_simple_ocr.csv

Simplified version of the electronic precinct dataset. Candidate data is extracted using OCR of
the electronic protocols instead of scraping the CEC website.

# cec_request_activity.csv

Dataset contains the activity for the 2024 Georgian Parliamentary Election, [as requested by
ISFED](https://isfed.ge/geo/gantskhadebebi/samartliani-archevnebis-dakvirvebit-saarchevno-ubnebis-mnishvnelovan-natsilshi-qali-da-katsi-amomrchevlebis-aqtivobis-doneebs-shoris-skhvaoba-atsdenilia-normalur-ganatsilebas-da-sheitsavs-praqtikulad-gamoritskhul-makhasiateblebs) from the Central Election Commission of Georgia.