# meet

## Description
Meet is a serverless, progressive web application (PWA) built with React using a test-driven development (TDD) technique. Meet uses the Google calendar API to fetch upcoming events for users specified by city. This app uses serverless to authorize users to be able to access event data from the Google Calendar API. 

## User Stories
- As a user, I should be able to filter events by city so that I can see the list of events that take place in that city.

- As a user, I should be able to see and hide an events details so that I can see view additional information on events I might be interested in.

- As a user, I should be able to see the number of events so that I know how many things are taking place that I can choose from.

- As a user, I should be able to use the app offline so that I do not have to rely on internet access to find something to do.

- As a user, I should see an app shortcut on my home screen so that I can easily access the app.

- As a user, I should see a chart showing the number of events by city so I can compare which city’s might be worth visiting.

## Scenarios
- Given user hasn't searched for any city
  When user opens the app
  Then user should see a list of all upcoming events
 
- Given the main page is open 
  When user starts typeing in the city textbox
  Then user should see a list of all upcoming events
 
- Given the user was typing "Berlin" in the search box and the list of suggested cities is showing
  When the user selects a city from the list
  Then their city should be changed to the selected city and the user should be able to see a list of upcoming events in that city only

- Given user is on the main page
  When user view a list of events
  Then user should initially see no more than the name of the event 
  
- Given user has seen an even that may be of interest
  When user clicks on that event
  Then user will see additional information specific to that event
  
- Given user has read the additional information on an expanded event
  When user indicates that they want to see less about that event
  Then xadditional information will collapse and user can continue scrolling through other events
  
- Given user has not specified a number of events they would like to view
  When user views a list of events
  Then user will see a list of 32 events by default
  
- Given user is viewing events on the app 
  When user indicates they would like to see more or less events
  Then user can changes the number of events they would like to see
  
- Given the user has opened the app
  When no internet connection is available
  Then user will be able to use app through use of cached data
  
- Given user has attempted to change settings
  When settings are incorrect
  Then an error will show
 
- Given user is searching for events
  When user would like to compare the number of events in a specified city
  Then a chart will be available to view the number of events in each city
