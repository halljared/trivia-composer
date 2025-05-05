# trivia-composer
Docker-compose manager and parent of the trivia frontend and backend repositories.

### 1. Clone the repository and initialize submodules

If you haven't cloned this repo yet:
`git clone --recurse-submodules <trivia-composer-url>`

If you've already cloned:
`git submodule update --init --recursive`

### 2. Add initial trivia data
Add a copy of the `trivia_data.sql` to `backend/sql/` so it can be loaded when the container is made.

### 3. Run the containers
`docker-compose up --build -d`

### 4. Load the page
The frontend is configured by default to run at http://localhost:3000/.