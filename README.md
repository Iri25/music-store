# music-store

A music store is providing services using a mobile app. The clients are able to view the available songs and add one or more of them to their list of favorites. The employees are able to manage the list of songs.

The following details are stored on the server side:
- Id - the internal song id. Integer value greater than zero.
- Title - the song title. A string of characters representing the song title.
- Description - a short description. A string of characters.
- Album - the name of the album. A string of characters.
- Genre - the song genre. A string of characters.
- Year - the release year. Integer value.

The application offers the following features:

● Client Section (separate activity - also available offline)

- View song genres from a list. Using the GET /genres call, the client will retrieve the list of genres available in the system. If offline, the app will display an offline message and a way to retry the connection and call.
- Using the GET/songs call by specifying a genre, retrieve the list of songs of that gender. Available online only.
- From the list of songs the client can select one song to retrieve and display all song details. Available online only.
- From the detail page the customer can mark the current song as favorite.
- View list of favorite song titles. The list is maintained on the device, on local storage, available offline.
