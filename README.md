# Web Scraping Challenge

Your challenge is to automate the process of extracting data from [**itdashboard.gov**](http://itdashboard.gov/).

- The bot should get a list of agencies and the amount of spending from the main page
- Click "**DIVE IN"** on the homepage to reveal the spend amounts for each agency
- Write the amounts to an excel file and call the sheet "**Agencies**".
- Then the bot should select one of the agencies, for example, National Science Foundation (this should be configured in a file or on a Robocloud)
- Going to the agency page scrape a table with all "**Individual Investments**" and write it to a new sheet in excel.
- If the "**UII**" column contains a link, open it and download PDF with Business Case (button "**Download Business Case PDF**")
- Your solution should be submitted and tested on [**Robocloud**](https://cloud.robocorp.com/).
- Store downloaded files and Excel sheet to the root of the `output` folder
- This task should take no more than 4 hours.
- If you reach 4 hours with tasks still remaining, please describe how in theory you would complete this challenge if more time was allowed.

### Running the Bot

```sh
echo "AGENCY_NAME='Department of Agriculture'" > ./.env
python3 -m venv venv
source venv/bin/activate
pip install -U pip wheel setuptools
pip install -r requirements.txt
python3 tasks.py
```
![Peek 2021-10-29 23-18](https://user-images.githubusercontent.com/40257388/139517137-1f4591e6-36e8-4e9e-abbe-27cb14519390.gif)
