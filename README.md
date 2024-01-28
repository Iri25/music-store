# music-store
Mobile client application developed in Kotlin with server developed in Node.js.

To run the server, execute:
```
npm install
npm start
```

A music store is providing services using a mobile app. The clients are able to view the available songs and add one or more of them to their list of favorites. The employees are able to manage the list of songs.

### The following details are stored on the server side:
- Id - the internal song id. Integer value greater than zero.
- Title - the song title. A string of characters representing the song title.
- Description - a short description. A string of characters.
- Album - the name of the album. A string of characters.
- Genre - the song genre. A string of characters.
- Year - the release year. Integer value.

### The application offers the following features:

● Client Section (separate activity - also available offline)
1. View song genres from a list. Using the GET/genres call, the client will retrieve the list of genres available in the system. If offline, the app will display an offline message and a way to retry the connection and call.
2. Using the GET/songs call by specifying a genre, retrieve the list of songs of that gender. Available online only.
3. From the list of songs the client can select one song to retrieve and display all song details. Available online only.
4. From the detail page the customer can mark the current song as favorite.
5. View list of favorite song titles. The list is maintained on the device, on local storage, available offline.

● Clerk's Section (separate activity - available online only)
1. Ascending tracklist by album and title. The list will be retrieved using same GET/all call. In this list, along with the title, album and genre, the application will also displays the year. Note that you are retrieving an unsorted list from the server.
2. Add a song. Using a POST/song call, sending the song object a new song will be added to the store list, on success the server will return the song object with the id field set.
3. Delete a song. Using DELETE/song call, by sending a valid song ID, server will remove the song. On success, a 200 OK status will be returned. 
