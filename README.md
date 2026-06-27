# Movie Recommendation System (Internship Task 4)

A simple content based movie recommender. You enter a movie you've
watched/liked, and it suggests other movies from the list that share
similar genres.

## Features

- Shows a numbered list of all available movies
- Takes a movie name as input (case-insensitive, ignores extra spaces)
- Finds other movies with overlapping genres and shows a match score
- Recommendations are sorted with the best match (highest score) first
- Handles the case where the entered movie isn't in the list

## How to use

1. Run the script, it will print the list of all movies with numbers.
2. When asked, type the name of a movie you liked (from the list).
3. It'll show you other movies that share genres with it, ranked by how
   many genres match.

Example: typing `Pathaan` will recommend other Action/Thriller/Sci-Fi
movies from the list, like `Kabir Singh` or `War`.

If you type a movie name that's not in the list, it'll just say it
couldn't find it.

## How it works

- Movie titles and their genres are stored in two separate lists
  (`movie_names` and `movie_genres`), matched up by index/position.
- The script searches for the entered title (case-insensitive) and grabs
  its genre list.
- It then loops through every other movie and counts how many genres
  match with the target movie's genres — that count is the "score".
- Movies with a score greater than 0 are kept as recommendations.
- These are then sorted manually (bubble sort style, swapping both the
  score and the matching name together) so the highest score comes
  first.
- Finally it prints out the sorted recommendations.
