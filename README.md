# Strava 'Spring into Songtember Challenge'
Placeholder for an idea if I can get to it in these next weeks. 

## Concept
Basic idea is to have Strava users add two hashtags to their activity descriptions uploaded to Strava during the month of September eg:

\#ItsMyLife
\#NoDoubt

And a photo or video of their impression/mood/dance to the song.


Then at the end of September, the users will be presented with:
- A video montage of their photos/videos to chosen songs
- Links to Spotify/Apple Music playlists to import.

## APIs
Strava API 

https://developers.strava.com/docs/reference/

Spotify API

https://developer.spotify.com/documentation/web-api

Apple Music API

https://developer.apple.com/documentation/applemusicapi/

## Workflow

### Strava-side

- Get authenticated athlete (getLoggedInAthlete)
- List Athlete Activities (getLoggedInAthleteActivities)
    - parameters:
      - before: 31st Sept
      - after: 1st Sept
      - pagination options (default is 1 page, 30 items)
- For activity in athlete activities:
  - Get activity (getActivityById)
    - Get "description" (hashtags for song/artist)
    - If photo count > 1
      -  get photos.urls{}

### Music-side

This is where I need to figure out how to compile playlists that can be listed to in Spotify/Apple Music. Unsure of approach on how to create a 'montage' video of users songs/images.
