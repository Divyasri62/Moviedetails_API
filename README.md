This is a Flask-based web application that fetches movie details from the OMDB API. You can search for a movie by its title and view details such as the Director, Actors, Awards, Plot, IMDB rating, and even the movie poster.

# Features
- Search for a movie by title
- View movie details (Director, Actors, Awards, Plot, IMDB rating)
- Display movie poster

# API Setup
You will need an OMDB API key to fetch movie details. You can obtain it from [OMDB API](http://www.omdbapi.com/apikey.aspx).

# Run Locally with Docker

1. Clone the repository:
   git clone https://github.com/Divyasri62/Moviedetails_API.git

2. Navigate to the project directory:
   cd movieAPI

3. Build the Docker image:
   docker build -t divya715/moviedetails_flaskapp .

4. Run the Docker container:
   docker run -d -p 5000:5000 divya715/moviedetails_flaskapp

5. Log in to Docker Hub:
   docker login

6. Push the Docker image to Docker Hub:
   docker push divya715/moviedetails_flaskapp

Access the app at http://localhost:5000


API Endpoints
Home Page:

Method: GET
URL: /
Description: Displays a form to input the movie title.
Get Movie Details:

Method: POST
URL: /get_movie
Parameters: title (string) - Movie title entered by the user.
Description: Fetches the movie details from OMDB API based on the title.
