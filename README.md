import pandas as pd

# ------------------- MOVIES -------------------
movies_data = {
    "movieId": list(range(1,26)),
    "title": [
        "Toy Story (1995)", "Jumanji (1995)", "Grumpier Old Men (1995)", "Waiting to Exhale (1995)",
        "Father of the Bride (1995)", "Heat (1995)", "Sabrina (1995)", "Tom and Huck (1995)",
        "Sudden Death (1995)", "GoldenEye (1995)", "American President (1995)",
        "Dracula: Dead and Loving It (1995)", "Balto (1995)", "Nixon (1995)",
        "Cutthroat Island (1995)", "Casino (1995)", "Sense and Sensibility (1995)",
        "Four Rooms (1995)", "Ace Ventura (1995)", "Money Train (1995)", "Get Shorty (1995)",
        "Copycat (1995)", "Shanghai Triad (1995)", "Leaving Las Vegas (1995)", "Othello (1995)"
    ],
    "genres": [
        "Adventure|Animation|Children", "Adventure|Fantasy", "Comedy|Romance", "Comedy|Drama", "Comedy",
        "Action|Crime|Thriller", "Comedy|Romance", "Adventure|Children", "Action", "Action|Adventure",
        "Comedy|Romance", "Comedy", "Adventure|Animation", "Drama", "Action|Adventure",
        "Crime|Drama", "Drama|Romance", "Comedy", "Comedy|Crime", "Action|Comedy",
        "Comedy|Crime", "Crime|Thriller", "Crime|Drama", "Drama|Romance", "Drama"
    ]
}

movies_df = pd.DataFrame(movies_data)
movies_df.to_excel("movies.xlsx", index=False)

# ------------------- RATINGS -------------------
ratings_data = {
    "userId": [1,1,1,2,2,3,3,4,4,5,5,6,6,7,7,8,8,9,9,10,10,11,11,12,12],
    "movieId": [1,2,3,1,4,5,6,1,7,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17],
    "rating": [4.0,3.5,2.0,5.0,3.0,4.5,3.5,2.5,4.0,3.0,4.0,3.5,5.0,4.0,2.5,3.5,4.0,5.0,4.5,3.0,4.0,2.5,3.5,4.5,4.0],
    "timestamp": [
        964982703,964981247,964982224,964983815,964981179,964982931,964983224,964980868,964982653,964981234,
        964982431,964983002,964982109,964981645,964983110,964982501,964981301,964983221,964982112,964981876,
        964983401,964982543,964981111,964982765,964983012
    ]
}

ratings_df = pd.DataFrame(ratings_data)
ratings_df.to_excel("ratings.xlsx", index=False)

print("movies.xlsx and ratings.xlsx created successfully!")
