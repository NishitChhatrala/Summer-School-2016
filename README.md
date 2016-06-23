# Summer-School-2016


Most of us can relate to kicking back on the couch and enjoying a movie with friends and family. In this project, you’ll build an app to allow users to discover the most popular movies playing. We will split the development of this app in two stages. First, let's talk about stage 1. In this stage you’ll build the core experience of your movies app.

Your app will:

Present the user with a grid arrangement of movie posters upon launch.
Allow the user to tap on a movie poster and transition to a details screen with additional information such as:
original title
movie poster image thumbnail
A plot synopsis (called overview in the api)
user rating (called vote_average in the api)
release date
Why this Project?
To become an Android developer, you must know how to bring particular mobile experiences to life. Specifically, you need to know how to build clean and compelling user interfaces (UIs), fetch data from network services, and optimize the experience for various mobile devices. You will hone these fundamental skills in this project.

By building this app, you will demonstrate your understanding of the foundational elements of programming for Android. Your app will communicate with the Internet and provide a responsive and delightful user experience.

You will fetch data from the Internet with theMovieDB API.
You will use adapters and custom list layouts to populate list views.
You will incorporate libraries to simplify the amount of code you need to write







Instructions about using API.

Working with the themoviedb.org API

A note on resolving poster paths with themoviedb.org API

You will notice that the API response provides a relative path to a movie poster image when you request the metadata for a specific movie.
For example, the poster path return for Interstellar is “/nBNZadXqJSdt05SHLqgT0HuC5Gm.jpg”
You will need to append a base path ahead of this relative path to build the complete url you will need to fetch the image using Picasso.
It’s constructed using 3 parts:
The base URL will look like: http://image.tmdb.org/t/p/.
Then you will need a ‘size’, which will be one of the following: "w92", "w154", "w185", "w342", "w500", "w780", or "original". For most phones we recommend using “w185”.
And finally the poster path returned by the query, in this case “/nBNZadXqJSdt05SHLqgT0HuC5Gm.jpg”
Combining these three parts gives us a final url of http://image.tmdb.org/t/p/w185//nBNZadXqJSdt05SHLqgT0HuC5Gm.jpg 
 
This is also explained explicitly in the API documentation for /configuration.
Stage 1 - API Hints

To fetch popular movies, you will use the API from themoviedb.org.
If you don’t already have an account, you will need to create one in order to request an API Key.
In your request for a key, state that your usage will be for educational/non-commercial use. You will also need to provide some personal information to complete the request. Once you submit your request, you should receive your key via email shortly after.
In order to request popular movies you will want to request data from the /movie/popular and /movie/top_rated endpoints. An API Key is required.
Once you obtain your key, you append it to your HTTP request as a URL parameter like so:
http://api.themoviedb.org/3/movie/popular?api_key=[YOUR_API_KEY]
You will extract the movie id from this request. You will need this in subsequent requests.
