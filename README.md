# DFIRRegex
A repo to centralize some of the regular expressions I've found useful over the course of my DFIR career

# Useful Regular Expressions

## URLs

`(http(s?)|ftp(s?)|afp):\/\/(((www\.)?\w+\.(com|org|net)|(\d{1,3}\.){3}\d{1,3}))`

## Email Addresses

`[A-Za-z0-9._%+-]+(%20|@)[A-Za-z0-9.-]+\.[A-Za-z]{2,4}`

## US Social Security Numbers

`\d{3}-\d{2}-\d{4}`

## Phone Numbers (Specify country)

`(\(\d{3}\)|\d{3})[-.\s]\d{3}[-.\s]\d{4}`

Links:

# To-Do
1. Add PowerGREP Library
2. fill out readme
3. Make Regex101 links for all the above to show how they work and don't work
4. add resources for regex
5. automate table of contents?
6. Add links for where expressiosn were found
