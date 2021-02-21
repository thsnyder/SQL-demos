# SQL-demos
SQL Portfolio
Database can be viewed/downloaded here: https://github.com/thsnyder/SQL-demos/blob/main/chinook.db

--Which tracks appeared in the most playlists? how many playlist did they appear in?
```
SELECT Name, Count(Name) AS "# of Playlists Song Appears in"
FROM playlist_track
JOIN tracks
	ON playlist_track.TrackId = tracks.TrackId
GROUP BY name
ORDER BY Count(Name) DESC
;
```
