# data_dump_dec_2023_polls
Dump of data scraped from election commission website for Dec 2023 polls

The data is available in the csv [all_candidates_data_2023.csv](all_candidates_data_2023.csv)

What the different fields in the csv represent is pretty self-explanatory.

Have put this out mainly to help academics, researchers etc. who aren't comfortable with coding.

Usually Ashoka university's [Lok Dhaba](https://lokdhaba.ashoka.edu.in/) would have put up the data by now, but in case they don't, hopefully this will be an acceptable substitute.

Given the structure of the data, you would still need considerable excel or stata or SPSS skills to do something analytical with the csv, but will leave that up to you.

The python script used to scrape the data [scrape_final_position.py](scrape_final_position.py) is also in the repo.

**Things to keep in mind**
1) `total_votes` field in [all_candidates_data_2023.csv](all_candidates_data_2023.csv) are the total votes *valid*. So rejected votes are not included. So it's votes for all the candidates + NOTA
2) The party short forms in `cand_party_short` are not unique. For example, 'National Janmandal Party', 'Navodaya Jantantrik Party', 'National Jagaran Party' and 'Nationalist Janshakti Party' all have the short form 'NJP' assigned to them. So be careful when using `cand_party_short`, use `cand_party` field for any analysis using party names.
