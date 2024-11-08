# 2024 Georgian Parliamentary Election (Round 1)

## Data

# cec_scrape_proportional.csv

Dataset contains the results of the 2024 Georgian Parliamentary Election for the proportional part of the election. 
The data was scraped from the Central Election Commission of Georgia's website (https://results.cec.gov.ge). 

All precincts, including electronic and traditional, are included in the dataset.

Columns with `_ocr_` are extracted using OCR of the protocols and may contain errors.

The dataset contains the following columns:

| Column Name                                     | Description                                                                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| district_id                                     | Unique identifier for the district associated with the precinct.                                                                         |
| district_alt_id                                 | Alternate identifier for the district if applicable.                                                                                     |
| division_id                                     | Unique identifier for the precinct.                                                                                                      |
| division_type                                   | Type of precinct (electronic/traditional).                                                                                               |
| address_1                                       | First line of the address associated with the precinct.                                                                                  |
| address_2                                       | Second line of the address, if applicable.                                                                                               |
| address_3                                       | Third line of the address, if applicable.                                                                                                |
| address_4                                       | Fourth line of the address, if applicable.                                                                                               |
| is_abroad                                       | Indicates if the precinct is located abroad (True/False).                                                                                |
| cancelled                                       | Indicates whether the election was cancelled (True/False).                                                                               |
| lat                                             | Latitude coordinate of the precinct.                                                                                                     |
| lng                                             | Longitude coordinate of the precinct.                                                                                                    |
| division_is_covid                               | Indicates if the division was created for COVID-19 patients (True/False).                                                                |
| election_type                                   | Type of election                                                                                                                         |
| total_registered_voters                         | Total number of registered voters in this district or location.                                                                          |
| total_registered_voters_men                     | Total number of registered male voters in this district or location.                                                                     |
| total_registered_voters_women                   | Total number of registered female voters in this district or location.                                                                   |
| election_numeric_id                             | Numeric identifier for the specific election.                                                                                            |
| protocols                                       | URL to the protocol.                                                                                                                     |
| total_votes                                     | Total valid votes cast in the election.                                                                                                  |
| participated_ocr_traditional                    | Number of voters who participated in the election (traditional protocol OCR).                                                            |
| participated_ocr_confidence_traditional         | Confidence level or reliability rating for the OCR.                                                                                      |
| invalid_ballots_ocr_traditional                 | Total number of invalid ballots in the election (traditional protocol OCR).                                                              |
| invalid_ballots_ocr_confidence_traditional      | Confidence level or reliability rating for the OCR.                                                                                      |
| participated_cec                                | Number of voters who participated according to the Central Election Commission (CEC).                                                    |
| participated_men_cec                            | Number of male voters who participated according to the CEC.                                                                             |
| participated_women_cec                          | Number of female voters who participated according to the CEC.                                                                           |
| invalid_ballots_ocr_confidence_electronic       | Confidence level or reliability rating for the OCR.                                                                                      |
| invalid_ballots_ocr_electronic                  | Total number of invalid ballots in the election (electronic protocol OCR).                                                               |
| participated_ocr_confidence_electronic          | Confidence level or reliability rating for the OCR.                                                                                      |
| participated_ocr_electronic                     | Number of voters who participated in the election (electronic protocol OCR).                                                             |
| c_participated                                  | First match for non-nan participated across all methods (participated_cec > participated_ocr_electronic > participated_ocr_traditional). |
| c_invalid_ballots                               | First match for non-nan invalid ballots across all methods (cec > electronic > traditional).                                             |
| CAND3                                           | Votes received by candidate 3 (Party for Unity and Development of Georgia).                                                              |
| CAND4                                           | Votes received by candidate 4 (Coalition for Change).                                                                                    |
| CAND5                                           | Votes received by candidate 5 (United National Movement).                                                                                |
| CAND6                                           | Votes received by candidate 6 (European Democrats).                                                                                      |
| CAND8                                           | Votes received by candidate 8 (Alliance of Patriots of Georgia).                                                                         |
| CAND9                                           | Votes received by candidate 9 (Strong Georgia–Lelo for People, for Freedom).                                                             |
| CAND10                                          | Votes received by candidate 10 (Labour Party of Georgia).                                                                                |
| CAND12                                          | Votes received by candidate 12 (Our United Georgia).                                                                                     |
| CAND16                                          | Votes received by candidate 16 (Change Georgia).                                                                                         |
| CAND17                                          | Votes received by candidate 17 (Georgia).                                                                                                |
| CAND20                                          | Votes received by candidate 20 (Free Georgia).                                                                                           |
| CAND21                                          | Votes received by candidate 21 (Tribune).                                                                                                |
| CAND23                                          | Votes received by candidate 23 (We).                                                                                                     |
| CAND25                                          | Votes received by candidate 25 (Gakharia For Georgia).                                                                                   |
| CAND26                                          | Votes received by candidate 26 (Left Alliance).                                                                                          |
| CAND27                                          | Votes received by candidate 27 (Georgian Unity).                                                                                         |
| CAND36                                          | Votes received by candidate 36 (Girchi).                                                                                                 |
| CAND41                                          | Votes received by candidate 41 (Georgian Dream).                                                                                         |

# cec_scrape_proportional_electronic.csv

Only electronic precincts are included in the dataset.

# cec_scrape_proportional_electronic_simple_ocr.csv

Simplified version of the electronic precinct dataset. Candidate vote data is extracted using OCR of
the electronic protocols instead of scraping the CEC website.

# cec_request_activity.csv

Dataset contains the activity for the 2024 Georgian Parliamentary Election, [as requested by
ISFED](https://isfed.ge/geo/gantskhadebebi/samartliani-archevnebis-dakvirvebit-saarchevno-ubnebis-mnishvnelovan-natsilshi-qali-da-katsi-amomrchevlebis-aqtivobis-doneebs-shoris-skhvaoba-atsdenilia-normalur-ganatsilebas-da-sheitsavs-praqtikulad-gamoritskhul-makhasiateblebs) from the Central Election Commission of Georgia.