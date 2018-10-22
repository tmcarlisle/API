## About

An application programming interface (API) is a clearly defined method of communicating between software systems. An API allows you to ask questions of another system and receive responses and pull data from the system. This lesson will help you understand the process of conducting an API request to download a particular subset of data from the Digital Public Library of America’s remote server. 
 
### Steps for this lesson:
* [Learn the basics of an API](#learn-the-basics-of-an-API)
* [Request an API key](#request-an-API-key) 
* [Submit an API request to DPLA](#submit-an-API-request-to-DPLA)
* [Convert downloaded data to a CSV file](#convert-download-data-to-a-CSV-file)

## 1. Basics of an Application Programming Interface

WATCH: “What is an API? Learn the Basics in 3 Minutes”
A beginner’s guide to the world of APIs with examples from Uber, Tinder, and Yelp https://uncubed.com/videos/uncubed/how-apis-work

READ: What is an API? A more in-depth definition
The Digital Public Library of America provides an good explanation of how API’s work and why they are so useful. https://pro.dp.la/developers/api-basics/

![uncubed video](https://github.com/tmcarlisle/API/blob/master/images/API_IntroVideo.png)

## 2. Request an API key
As part of the assignment you will need to request an API key from DPLA. To accomplish this task you will request the key using the command line on your computer, which is an under-the-hood view of a computer. Here are the steps to request an API key from your computer’s command line. 

### For Windows users:
* Click on Start in bottom left of screen> In the search box type “command” > Click on “Command Prompt” listed in the pull-up menu.
* At the [c:\...] prompt, paste the following url and add your own email address in place of the example address: https://api.dp.la/v2/api_key/YOUR_EMAIL@example.com 
* DPLA (info@dp.la) will send you an API key via email which will be a long string of numbers and letters like this: 99ca63b3cfd9d1721a712f2bea9 (if you don’t receive the message check your junk mail) 

<img src="API_windows_shell.png" alt="windows" width="200"/>

### For MAC users:
* Open Finder > Open your Applications folder > Open Utilities folder > Open Terminal
* At the Terminal’s prompt, paste the following url and add your own email address in place of the example address: https://api.dp.la/v2/api_key/YOUR_EMAIL@example.com 
* DPLA (info@dp.la) will send you an API key via email which will be a long string of numbers and letters like this: 99ca63b3cfd9d1721a712f2bea9 (if you don’t receive the message check your junk mail) 

## 3. Submit an API request to the Digital Public Library of America
Once you have an API key you are able to submit an API request to DPLA and download the descriptive metadata from its collections. You can use the base URL of the API to search for any number of items, collections, or even search a particular field like title.  This is where the fun begins! To learn how to do this: 

READ: One-page guide on the different kinds requests that you can make https://pro.dp.la/developers/requests 

Example:  To find all items in DPLA that has the word “kittens” in any field, here is the URL I would add to a browser: https://api.dp.la/v2/items?q=kitten&api_key=

But something is missing from the request URL above. What is it? 
My unique api key is missing. Here what the full request would look like using a sample key.
https://api.dp.la/v2/items?q=dog&sort_by=sourceResource.title&api_key=85399ca63b3

Don’t forget to add YOUR unique API key to the end of the request as I have done in the above example.

API request

JSON data received from API request

## 4. Convert JSON data to CSV file
The data that you receive from DPLA is in JSON format (image above) and thus difficult to read or analyze. Fortunately,  JSON can be converted to Excel (XLSX) format using a web accessible converter tool.  

Follow these steps:

* Copy the JSON text that you received from DPLA
* Open a new browser tab or window and go to https://json-csv.com/ 
* Paste the JSON text into the converter box
* Click on the XLSX button (located just right of the green “DOWNLOAD CSV” button)
* You will be prompted to download the XLSX file
* Name the file and download it to your computer


[Return to Top](#about)
