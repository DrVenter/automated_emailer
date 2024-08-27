# Automated Emailer

## Motivation
I had previously developed a [script to scrape email addresses from Pubmed](https://github.com/DrVenter/pubmed_scraper/blob/main/README.md) which would allow sales representative to find potential clients. However, it is  difficult and slow to manually email custom messages to every individual.

## Aim
Develop a script to send custom emails to professors in a database that contains their email address, name, and the title of an article they published.

## Method
This project uses Python and Google's Gmail API to iterate through a database and send custom emails depending on the authors name and the article title. Once the email is sent, the email address is saved to a file which is checked before an email is sent; this prevents multiple emails being sent to the same address.

## Installation and Use

### Initial Set-Up
1. Clone the respository 
```bash
git clone https://github.com/DrVenter/automated_emailer.git 
```
2. Navigate to the project directory
```bash
cd automated_emailer
```
3. Create a virtual environment
```bash
python -m venv venv
```
4. Activate the virtual environment
```bash
source venv/bin/activate
```
5. Install the dependencies
```bash
pip install -r requirements.txt
```

### Create a Google Cloud Project
1. Go to [Google Cloud] (https://cloud.google.com/), navigate to Console, and create a new project (Select a project → New Project).
2. Name the project "Automated Emailer" and click on 'Create'.
3. Navigate to APIs & Services → Library
4. Select GMail API → Enable
5. Navigate to 0Auth consent screen, select 'External' and then 'Create'.
6. Fill in App information i.e App name. User support email, Email Addresses.
7. Click 'SAVE AND CONTINUE'.
8. Click 'SAVE AND CONTINUE' again for Scopes, Test users
9. Click 'BACK TO DASHBOARD'.
10. Navigate to Credentials → + CREATE CREDENTIALS → 0Auth client ID
11. For 'Application type', click on 'Desktop app' then click 'CREATE'
12. Download the JSON file to the automated_emailer directory.
13. Copy the path of the JSON file to the CREDENTIALS_PATH variable in the notebook/script.

### Running the Script
1. Navigate to the script directory
```bash
cd automated_emailer/notebooks
```
2. Open the notebook in Visual Studio Code
```bash
code automated_emailer.ipynb
```
3. Run through the script and change the email address and contents.

## Outcomes
The script was able to very quickly send several emails in a short of time. As a test, I sent 176 emails to authors asking for a copy of their research paper and I received about 72 replies.

## Contact
Colin Venter - ventercolin3@gmail.com

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Disclaimer
I acknowledge that ChatGPT was used to help create this project. However, the problem was mine and I did put the code together.

## Lessons Learned
While developing this project, I gained new knowledge in these areas:

### 1. How to Handle Google's API
- Understanding some of the code for handling the API is still confusing but I have created a Google Cloud Project so many times during this project.

### 2. How to use Git
- Understanding how to use Git, upload files onto GitHub, how to handle branches, and how to use a .gitignore file to prevent personal documents from being tracked.