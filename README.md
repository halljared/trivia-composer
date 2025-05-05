# trivia-composer
Docker-compose manager and parent of the trivia frontend and backend repositories.

### 1. Add initial trivia data
Add a copy of the `trivia_data.sql` to `backend/sql/` so it can be loaded when the container is made.

### 2. Run the containers
`docker-compose up --build -d`

### 3. Load the page
The frontend is configured by default to run at http://localhost:3000/.