# SQL-inlämning — Diskografi

**Namn:** Max Svensson
**Artist:** Joey Bada$$
**Datum:** 2026-10-13

---

> Lägg länk till eller bild på ditt ER-diagram här:
> `[ER-diagram](er_diagram.png)`

---

## 1. Skapa databasen — CREATE TABLE

```sql
--- skriv din SQL-kod här ---

CREATE TABLE artist (
                        artist_id INTEGER NOT NULL PRIMARY KEY,
                        first_name VARCHAR(50),
                        last_name VARCHAR(50),
                        stage_name VARCHAR(50),
                        origin VARCHAR(50),
                        active_since INTEGER
);

CREATE TABLE genre (
                       genre_id INTEGER NOT NULL PRIMARY KEY,
                       genre VARCHAR(50)
);

CREATE TABLE albums (
                        album_id INTEGER NOT NULL PRIMARY KEY,
                        artist_id INTEGER,
                        album_name VARCHAR(255),
                        release_date INTEGER,
                        genre_id INTEGER,
                        cover_image_url VARCHAR(500),
                        FOREIGN KEY (artist_id) REFERENCES artist(artist_id),
                        FOREIGN KEY (genre_id) REFERENCES genre(genre_id)
);

CREATE TABLE songs (
                       song_id INTEGER NOT NULL PRIMARY KEY,
                       album_id INTEGER,
                       song_name VARCHAR(255),
                       track_number INTEGER,
                       duration_seconds INTEGER,
                       is_single BOOLEAN,
                       FOREIGN KEY (album_id) REFERENCES albums(album_id)
);

```

---

## 2. Seeda med data — INSERT

```sql
--- skriv din SQL-kod här ---

INSERT INTO artist (artist_id, first_name, last_name, stage_name, origin, active_since)
VALUES (1, 'Jermaine', 'Cole', 'J. Cole', 'Fayetteville, North Carolina', 2007);

INSERT INTO genre (genre_id, genre)
VALUES (1, 'Hip-Hop'),
       (2, 'East Coast Hip-Hop'),
       (3, 'Conscious Hip-Hop');

INSERT INTO albums (album_id, artist_id, album_name, release_date, genre_id, cover_image_url)
VALUES (1, 1, '2014 Forest Hills Drive', 2014, 1, 'https://upload.wikimedia.org/wikipedia/en/2/2a/2014ForestHillsDrive.jpg'),
       (2, 1, 'Might Delete Later', 2024, 2, 'https://upload.wikimedia.org/wikipedia/en/2/22/J._Cole_-_Might_Delete_Later.png'),
       (3, 1, 'Born Sinner', 2013, 3, 'https://upload.wikimedia.org/wikipedia/en/7/73/J._Cole_-_Born_Sinner_cover.png');

```

---

## 3. Söka — SELECT

```sql
--- query 1: Lista alla album, sorterade efter år ---


--- query 2: Lista alla låtar på ett specifikt album ---


--- query 3: Antal låtar per album ---


--- query 4: Längsta låten ---


--- query 5: Alla låtar sorterade alfabetiskt ---

```

---

## 4. Lägg till en ny rad — INSERT

```sql
--- lägg till ett nytt album eller en ny låt ---

```

---

## 5. Ta bort en rad — DELETE

```sql
--- ta bort en rad ur valfri tabell ---

```

---

## 6. Uppdatera en rad — UPDATE

```sql
--- uppdatera minst en rad i valfri tabell ---

```

---

## 7. VG-queries (om du siktar på VG)

```sql
--- query 6: Snittlängd på låtar per album ---


--- query 7: Albumet med flest låtar ---


--- query 8: Alla låtar längre än 4 minuter (240 sekunder), med albumtitel ---

```
