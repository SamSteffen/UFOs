# UFO Sightings Data
## Overview
The following outlines the creation of a web-based visualization and analysis tool for filtering UFO sighting data using JavaScript, Bootstrap, HTML and CSS. 

To help a client, Dana, present JSON data on UFO sightings and allow users to easily peruse it, the following steps were taken: 
1. We created an html script ("index.html") that included a button enabling the user to filter the data by the date value. 
2. We wrote a javaScript code ("app.js") containing the functions "buildTable ()" and "handleClick()" that would allow our webpage to create a table of the JSON data upon loading, and then allow the user to filter it by the "date" property using a clickable button.

To allow for greater specification in filtering searches, a request was presented to provide additional filter inputs. This required refactoring of our initial JavaScript code.

## Results
To refactor our webpage to include filtering capabilities based on additional user input, we first modified our "index.html" code by removing the user-facing button that activated the 'handleClick' function of the "app.js" script. We then added html code to our "index.html" file, creating input boxes that could accommodate "city", "state", "country", and "shape" parameters, in addition to our original "date" parameter, as inputs. 

Once our html was updated, our webpage filter section resembled the following:

<img width="234" alt="Input_boxes" src="https://user-images.githubusercontent.com/104729703/185286893-0f482992-699e-4697-9243-42cede7295b9.png">

The table we created allows for a wide range of specification in filtering the dataset. If a user wanted to view all of the UFO sightings from any single search parameter they could do so by utilizing any single input box, or a variety of them, in concert:

- Say you wanted to find all the UFO sightings in the dataset that were reported on "1/5/2010"; you could do so by entering the date as such in the "Enter Date" field:

<img width="943" alt="date" src="https://user-images.githubusercontent.com/104729703/185286913-8bc65c93-48eb-4581-a3d3-3225f4c598ef.png">


- Say you wanted to find all the UFO sightings in the dataset that were reported in "st. louis"; you could do so by entering the city as such in the "Enter a City" field:

<img width="932" alt="city" src="https://user-images.githubusercontent.com/104729703/185286952-bc374454-4ea4-48b9-909b-c2092e0f9691.png">

- Say you wanted to find all the UFO sightings in the dataset that were reported from Pennsylvania; you could do so by entering the state as "pa" in the "Enter a State" field:

<img width="940" alt="state" src="https://user-images.githubusercontent.com/104729703/185286984-263ceaab-6b83-4a26-af68-690312cb40f2.png">

- Say you wanted to find all the UFO sightings in the dataset that were reported from Canada; you could do so by entering the country as "ca" in the "Enter a Country" field:

<img width="929" alt="country" src="https://user-images.githubusercontent.com/104729703/185287010-09953d36-9358-44af-81ee-5a3e11c946e8.png">

- Say you wanted to find all the UFO sightings in the dataset that were reported as circular in shape; you could do so by entering the shape as "circle" in the "Enter a Shape" field:

<img width="928" alt="shape" src="https://user-images.githubusercontent.com/104729703/185287035-9f22baba-1e81-43a8-a0c5-973003e263b5.png">

Additionally, the input boxes we've created also allow for increased specification. If a city-state-country-shape combination is desired, they can all be entered simultaneously to return the data where all parameters are met.

Alternatively, if only some of the parameters are known or wanted, they can be entered in the respective fields to achieve the desired results. Say for instance you wanted to see all the data that was reported in the state of Florida on 1/11/2010; you could enter just the date "1/11/2010" and the state "fl" to return the data desired:

<img width="928" alt="mixed" src="https://user-images.githubusercontent.com/104729703/185287061-e0e3a0f8-364c-4197-bbfd-3bedceb802ba.png">

## Summary
While the search parameters we've enabled the user to input allow for data inquiries as broad or narrow as the imagination allows, it's important to point out that one key limitation in our program, the way it's written, is that it will only capture an EXACT input match for each of the data properties. Say, for instance, you wanted to see all of the UFO sightings in the state of Florida and you entered the word "Florida" in the search box. This would not return any results becuase our JavaScript is only looking for EXACT text matches, case-size and all.

With this in mind, several ideas for further code refactoring present themselves, among them, these:
- Refactoring the code to allow for returns in spite of case sensitivity or spelling;
- Creating notes in the html to appear on the webpage about how the terms should be entered in the respective search boxes to avoid blind searches that return no results (i.e. "Enter a date between 1/1/2010 and 1/13/2010" or "Enter a country('us' or 'ca')", etc.);
- Adding additional input boxes that will search by the "duration" property or by keywords from the "comment" properties of the data;
- Supplying additional print "messages" to return to the user in the event that no data is returned from the search.
