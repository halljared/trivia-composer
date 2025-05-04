# trivia-composer
Docker-compose manager and parent of the trivia frontend and backend repositories.

## Add initial trivia data
Add a copy of the `trivia_data.sql` to `backend/sql/` so it can be loaded when the container is made.

## Run the containers
`docker-compose up --build -d`

## Load the page
The frontend is configured by default to run at http://localhost:3000/.