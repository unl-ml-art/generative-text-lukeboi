# Project 1 Generative Text

Luke Farritor, yourcontact@unl.edu

## Abstract

One of my favorite corners of the internet is [Marginal Revoultion](https://marginalrevolution.com/) (MR), a blog by economists Tyler Cowen and Alex Tabarrok. The authors share a few posts a day covering a wide range of topics from economics, art, politics, philosophy and everything in between. MR has a comments section, which ranges from high quality discussion to low quality jokes and everything in between. I finetune GPT-2 to generate MR comments based on real posts. Creating a datset was easy - MR has had comments ranging back over 15 years. I had difficulty scraping automatically, as their antispam seemed to block my scripts (even when sending requests very slowly). Instead, I just manually saved a large number of comments pages to a directory. As a strech goal, I could create a seperate lookalike/parody website showcasing the fake comments, with a disclaimer that the site is not affiliated with the real MR.

## Model/Data

Trained data is in MR Scrapes as saved HTML files
Finetuned models are not included in repo (size constraints) but are automatically downloaded as needed

## Code
notebooks:
mr scrapes / parser -> scrapes the comments sections and puts that dataset of comments into /dataset.txt
train -> finetunes GPT2 on dataset.txt
inference -> runs intference and puts output in output.txt
create html -> creates HTML page from plaintext output in output.txt

## Results

see results in Full generation.html

## Technical Notes

used beautifulsoup which seems like a nice tool
i should clean this up once it's not 4am

## Reference

  - [MARGINAL REVOULTION ITSELF](marginalrevoultion.com)
