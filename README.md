# meet app:

meet is a serverless progressive web app (PWA) that allows users to search for upcoming events in different locations.

FEATURE 2: SHOW/HIDE AN EVENT'S DETAILS
----------------
As a user, 
I should be able to show or hide each event's details
So that I can get only the information I really need and not fill my screen with unnecessary details.

-Scenario 1: An event element is collapsed by default

Given: all the app data has loaded and user has opened the app
When: user has opened the app and navigated to a list of events by city
Then: the event information details are hidden by default.

-Scenario 2: User can expand an event to see its details

Given: all app data has loaded and user has opened the app 
When: the user clicks or taps on the event UI
Then: the box should expand to display event details.

-Scenario 3: User can collapse an event to hide its details

Given: all app data has loaded and user has opened the app
When: the user clicks or taps a second time on the same event
Then: the box should collapse to hide details.

FEATURE 3: SPECIFY NUMBER OF EVENTS
----------------
As a user,
I should be able to choose the specific number of events to display
So that I can narrow down my choices to the ones I'm most interested in.

-Scenario 1: When user hasn’t specified a number, 32 is the default number

Given: all app data has loaded and user has opened the app
When: the list of events loads after the user chooses the city
Then: the list should show 32 events.

-Scenario 2: User can change the number of events they want to see

Given: all app data has loaded, and user has chosen the city
When: user updates the widget controlling number of events
Then: the number of events should match the number the user has input.

FEATURE 4: USE THE APP WHEN OFFLINE
----------------
As a user,
I should be able to use the app offline
So that the app works seamlessly regardless of location, and I can pull up event information without needing a data or wifi connection.

-Scenario 1: Show cached data when there’s no internet connection

Given: the user is not connected to any internet service
When: the user opens the app
Then: the app should load previously loaded data from the cache rather than fetching it from a server over a connection.

-Scenario 2: Show error when user changes the settings (city, time range)

Given: the user is not connected to any internet service
When: the user tries to change settings
Then: an error message should appear.

FEATURE 5: DATA VISUALIZATION
----------------
As a user,
I should be able to view a graph of the data in the app
So that I can more easily understand where there are more or less events happening.

-Scenario 1: Show a chart with the number of upcoming events in each city

Given: the user has opened the app and all app data has loaded for a specific city
When: the user clicks or taps on the "chart" icon
Then: a data visualization chart will appear.
