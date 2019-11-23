# WhatsNext
**PROBLEM**
  - Difficult to recommend music to friends
  - When you are at a party it is difficult to get your music played 
  - People don't have a voice in choosing their song


**DATA DESIGN**
  - SignUp View controller
  - https://stdlib.com/ for Twillio
  - Like Queue in request
  - Firebase
      - User Collection
         * Name
         * Email
         * Phone number
         * Profile pic
      - Host Collection
         * Host user
         * Geo Location of Event
         * Rules for Event 
         * Sub Collection for Song Queue
            - Genre 
            - Timestamp added
            - Likes/Dislikes 
            - User sent/Profile

**ARCHITECTURE DESIGN**
Sign in/ Sign up
Users collection
Check for duplicate users
Declare music subscription service
Create Event
Create a new document in the hosts collection 
Populate geo location
Host user
Rules
Create sub collection for song queue
Create a token for host user
Use token to set up peer to peer connection 
Multi peer connectivity framework
Twilio
Create custom event number
Link event number to the token
Users connect to event
User connects to spotify/apple music API and searches for song


Send song as document in queue subcollection
Create new song document and add to queue subcollection for host event
Host looks at song queue
Sort algorithm
Sort by timestamp
FIFO
Sort by likes
Query order by likes(descending)
Host can swipe and change order at any time
Host can delete songs from queue at any time
Auto Add btn
Takes the subcollection queue and using music subscription service creates playlist in music app
https://developer.apple.com/documentation/applemusicapi/create_a_new_library_playlist
https://developer.apple.com/documentation/applemusicapi/add_tracks_to_a_library_playlist
https://developer.spotify.com/documentation/web-api/reference/playlists/create-playlist/
https://developer.spotify.com/documentation/web-api/reference/playlists/add-tracks-to-playlist/
