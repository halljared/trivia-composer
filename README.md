
# trivia-composer
Repository that manages docker-compose setup for my trivia frontend and backend repositories.

## Running the app

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

## Environment Info
The app is split up into 3 docker containers:
 * **db**: Runs postgres. Is initialized with trivia questions.
 * **backend**: Runs an API server that handles authentication and fetching data for the frontend.
 * **frontend**: Builds the frontend code and runs an apache server that serves the frontend. The apache server also reverse-proxies API requests (requests that begin with `api`) to the `backend` container.

Individual configuration files for the `backend` and `frontend` are found in their respective submodules.

## Miscellaneous
Commands for managing the docker containers:
 * **`docker-compose down -v`** - Stop and remove all networks/containers/volumes
 * **`docker-compose up --build -d`** Build and run the containers
 * **`docker-compose up -d`** Run containers that were built previously.