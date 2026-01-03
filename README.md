# Postman API Automation Integration with GitHub Actions ##
This repository is a POC demonstration for integrating Postman tests with GitHub Actions. The tests are written in Postman and executed on a virtual machine using Newman and the newman-reporter-htmlextra library.

GitHub Actions triggers the project execution on every push to the main branch. The workflow can also be triggered manually using workflow_dispatch, and a scheduled run is configured using a CRON job.

The HTML report is archived and available in the Artifacts section for download. Additionally, the latest report can be viewed directly on the GitHub Pages site: https://kumar-vasanth.github.io/Phoenix-In-warranty-Flow-Collection/ The Latest report is mailed to the team members using GMAIL SMTP.

About Me
Hi, My name is vasanth kumar sadhu having 4.6 years of  Automation testing experience. My Skillset includes UI Automation with Selenium WebDriver for UI Testing and for API Testing I use Rest Assured and Postman.


# Testing Coverage #
1.Happy Flow Testing
2.Negative Testing and Edge Case Testing
3.Token Testing
4.Data Driven Testing with CSV
5.Schema Validation
6.Secrets Management with GitHub Secrets
 # Tech Stack #
1.Postman
2.Nodejs 22v
3.Newman
4.Newman-reporter-htmlextra
5.GitHub Actions
6.Gmail SMTP
7.GitHub Pages
8.CSV for Data Driven Testing
9.AWS-EC2 instance for self-hosted GitHub runner.
10.GitHub Pgaes
You can directly view the latest test report of the Postman test at the GitHub Page Link: https://kumar-vasanth.github.io/Phoenix-In-warranty-Flow-Collection/

HTML Report
The report will be created in the Newman folder Postman Report

# Project Structure ##
Vasanth's Phoenix Inwarranty Flow
├─ Inwarranty-flow Collection.postman_collection with External Data API.json #Collection FIle
├─ QA.postman_environment.json #Envoirnment File
└─ testdata.csv #Test Data File

How to run the Project?
You can run the project on your local system for that:

Clone the project on Local System: https://github.com/kumar-vasanth/Phoenix-In-warranty-Flow-Collection.git
Install Node.js and NPM from: https://nodejs.org/en
Install Newman using: npm install -g newman
Install Newman-reporter-htmlextra: npm install -g newman-reporter-htmlextra
Run the Newman command:
            newman run 'Inwarranty-flow Collection.postman_collection with External Data API.json' \
           -e QA.postman_environment.json \
           -d testdata.csv \
           -r cli,htmlextra \
           --reporter-htmlextra-export ./newman/index.html
