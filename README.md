# Rulemaking-Comments
The goal is to create a spreadsheet of the important comments from federal registry rules and policies. 

## Functionality
The code is meant to call the federal registry api through http requests and then in turn collect the comments. When an agency requests comments on a proposed rule there are often thousands of comments. The only way to read all the comments is to use the api. The federal registry also has outlined on the website how to access all of the api. Using the docket number of the selected federal registry publication you can access a large amount of the information on the documents and comments of the documents. 

## Current status
I ran into a major issue during development: to call the next chunk of comments with the url request you use the lastModified date from the last comment in the previous set. However, when called with the lastModified date, the first comment in entry would skip nearly a whole day which is NOT GOOD. This results in skipping thousands of comments and missing important companies' inputs. No fix has been discovered yet

## Files
The comments_to_spreadsheet file is the original file I made with the conversion to a spreadsheet with the comments. It also turns the attachments of the comments into text with a PDF reader and adds that to the spreadsheet. That notebook ended being messy and a little more than what we needed so I created the comments_to_spread_clean. This notebook looks to do the same thing in a cleaner way. It was in this notebook that I realized the API was skipping nearly a whole day with each call, so it is not finished. The first thing I when coming to this code is trying to fix that issue. 
