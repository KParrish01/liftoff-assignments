# Project Outline
For this assignment, you will submit a high-level outline of your project. This can, and likely will, change over time. In particular, your mentor will provide direction and feedback to help sharpen your ideas. So don't worry if you feel unsure about some aspects of the outline or if you have to change some things later.

## Assignment Description
[Project Outline Assignment](https://education.launchcode.org/liftoff/modules/assignments/project-outline)

## Submission Instructions

### Overview
The project will be a professional tool to automate the review of bank loan portfolios and the analysis of (commercial) loans (and possibly at a later point also loan underwriting). The app will take standardized loan data banks can easily download from their systems (called "Examiner Downloads"), extract information from the data to create line sheets for auditors, and perform basic analyses for each loan. The goal is to speed up the auditors' work, reduce errors, and lessen the need for edits. 

The motivation for the project came from me having a strong dislike for repetitive work when performing loan reviews. It is designed to help auditors, bank examiners, bankers, financial analysts and economists more efficiently pinpoint a bank's loan portfolio's strengths and weaknesses and conduct loan reviews. (At a later point, the project might be expanded to add tools to help loan underwriting.)


## Features

1. Read in Examiner Download: For Audit Manager to be able to work with data, read bank data ("Examiner Download" - text file) into MySQL and clean up data.
   1. Change fixed-width TXT file without headers into usable CSV file to analyse
   2. Display data to check for potential issues with original data
   3. Upload CSV file and change fields into appropriate data types (numbers and dates in addition to text)
   4. Export file to CSV and/or Excel document
2. Choose Sample: For Audit Manager to choose a sample of loans with certain features, extract loans from above database.
   1. Provide various pre-programmed risk-focused 'boxed' sampling options
   2. Print report with sampled loans (showing at least borrower, loan amounts and account numbers)
   3. Later release: Customized data analysis (for example, direct links from table in 1b)
   4. Save sample in LPA to print line sheets
3. Create Line Sheets: For Audit Manager to prepare loans to be audited, create line sheets and populate them with data extracted from above database (including some calculations).
   1. Set up line sheets and populate them with data from Examiner Download
   2. Export the line sheets to Excel for further analysis (or possibly to PDF for printing)
   3. Later release: Allow for Line Sheets to be worked within LPA
4. Set up library of financial methods such as amortization, NPV, debt-service calculation to use in this and other programs.
5. Future Release: Analyze Financials: For Auditor to analyze financials for each loan (read or typed in separately), provide financial pages with some pre-set calculations.
6. Future Release: Create Summary Reports: For Audit Manager to create reports with summarized findings (technical exceptions, summary review findings, ...), set up tables with summary of review.
7. Future Release: For Audit Manager to analyze loans on an aggregate basis (could be used for Allowance for Loan and Lease Loss (ALLL) analysis, Board of Directors reports, due diligence, audits and possibly also for CECL?), provide pre-set calculations.
8. Future Release: For Auditors to easier work loans, add external public data to the loan file such as macro economic data to make predictions for loans based on industry (possibly also industry databases such as Dunn & Bradstreet).
9. Future Release: For Audit Manager to to create risk estimates and projections, add external public macro data and Uniform Bank Performance Report (UBPR).
10. Future Release: For Auditors to easier work loans, pull outside public information into app and help analyze loans (e.g. UCC filings, appraisal estimates, company information, business search (date company formed), recordings of deeds and mortgages, etc.)
11. Future Release: For Auditors to easier work loans, analyze bank loan documents (from separate system).
12. Future Release: Possibly User login: The App will probably live behind firewalls on a secure computer without access to the public, but due to the confidentiality of the data, User Login and Authentication might still need to be considered.
13. Future Release: At a later later point: Would be great to use some AI to help underwrite loans/industries. - Goal would be to at some point allow for "real time data" commercial underwriting instead of the current "driving while looking in the rear view mirror" approach to underwriting based on 1-3-year old financial data.


## Technologies

* Java
* Spring Boot
* MySQL
* Hibernate
* Thymeleaf 
  
### What I'll Have to Learn
Early on, I need to learn MySQL EER to draft the relationship between the datatabases.

I will need to learn how to read a large text file that should have data in columns with standardized labels into MySQL, but will need to check for missing columns and check for possible errors in the original data and allow for clean up of the data. Once the data is "clean" and in MySQL, I will need to learn to manipulate the data to query loans with certain features, pull that information into separate tables that create the basis for line sheets, perform certain calculations, and populate line sheets. Ideally, the line sheets would still be within the system, would allow for text and data to be added manually by an auditor, be printed out efficiently into a PDF and transferred into Excel, yet stay within the project to allow for the creation of summary reports of the findings.

Learn how to deal with databases with many empty cells.
Learn how to change data types from Strings to Doubles, Integers and Dates.
Learn how to persist databases uploaded from CSV files.

At a later point, I would like to learn how to pull public information from the Internet into the system to allow for the automation of additional analyses. (And yet at a later point, the information from a bank's loan documentation system could be added, if the system is set up appropriately - which may not be in my control though, thus may not be realistic in the near future.)

Moreover, all of above needs to keep in mind that I am dealing with highly confidential information.

### Project Tracker
https://trello.com/invite/b/2UFoKdGC/f80c08d5525b915d082e238b5a4858c6/liftoff-project-board-klara
(https://trello.com/b/dIsStOiO/liftoff-project)
