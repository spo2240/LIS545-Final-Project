The files included in this dataset are as follows (descriptions adapted from https://www.kaggle.com/datasets/furkanark/myanimelist-top-10000-anime-dataset):

## anime.csv
The central table containing general information and statistics for each anime. All other tables link back to this one. The variables are as follows:
1. anime_id: Unique identifier for each anime title (Primary Key).
2. title: The official name of the anime.
3. score: Average user rating on MyAnimeList (0-10).
4. rank: Global ranking based on score.
5. popularity: Ranking based on the number of members.
6. members: Total number of users following the anime.
7. synopsis: A brief plot summary of the anime.
8. start_date: The date the anime first aired (ISO-8601).
9. end_date: The date the anime finished airing (ISO-8601).
10. type: Media format (TV, Movie, OVA, ONA, Special).
11. episodes: Total number of episodes.
12. image_url: Link to the official poster image.

## entities.csv
A centralized table for names and images. Use this to map IDs from other tables to their actual names. The variables are as follows:
1. entity_id: Unique identifier for the entity (Primary Key).
2. entity_type: Category of the entity (studio, character, staff, voice_actor).
3. name: Full name of the person, character, or organization.
4. image_url: Link to the official image of the entity.

## anime_genres.csv
Establishes the relationship between anime titles and their associated genres or themes. The variables are as follows:
1. anime_id: Foreign key linking to anime.csv.
2. genre: The specific genre or theme (e.g., Action, Sci-Fi).

## anime_characters.csv
Lists which characters appear in which anime and defines their importance. The variables are as follows:
1. anime_id: Foreign key linking to anime.csv.
2. character_id: Foreign key linking to entity_id in entities.csv.
3. role: Character prominence in the story (Main or Supporting).

## anime_staff.csv
Lists the professional staff members involved in the production of the anime. The variables are as follows:
1. anime_id: Foreign key linking to anime.csv.
2. person_id: Foreign key linking to entity_id in entities.csv.
3. role: The person's professional role (e.g., Director, Producer, Script).

## anime_companies.csv
Lists the studios and production companies behind each anime title. The variables are as follows:
1. anime_id: Foreign key linking to anime.csv.
2. company_id: Foreign key linking to entity_id in entities.csv.
3. role: The company's role (Studio, Producer, or Licensor).

## anime_voice_actors.csv
Links characters to the specific voice actors who portrayed them. The variables are as follows:
1. character_id: Foreign key linking to the character's entity_id in entities.csv.
2. person_id: Foreign key linking to the voice actor's entity_id in entities.csv.
3. language: The language of the performance (e.g., Japanese).

## dataset-metadata.json
Metadata for the dataset.

## DataCite Metadata Schema XML
This file contains the DataCite Metadata Schema for the above documents.

## finalreport.pdf
Put in elements.....

