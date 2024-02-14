# First Time Setup

## Files Server

Use this to run a local file-upload server.

# Setup

- Start the server with `pdm run files`
- In the `pdf` project, find the `.env` file and change the `UPLOAD_URL` line to the following: `UPLOAD_URL=http://127.0.0.1:8050`


## Web Server

```
# Create a virtual environment
pdm venv create

# Install dependencies
pdm install

# Initialize the database
pdm run init-db

```

# Running the app

There are three separate processes that need to be running for the app to work: the server, the worker, and Redis.

If you stop any of these processes, you will need to start them back up!

Commands to start each are listed below. If you need to stop them, select the terminal window the process is running in and press Control-C

### To run the Python server

Open a new terminal window and activate virtual environment after checking the command:

```
pdm venv activate
```

Then:

```
pdm run dev
```

### To run the worker

Open a new terminal window and activate virtual environment after checking the command:

```
pdm venv activate
```

Then:

```
pdm run devworker
```

### To run Redis

```
redis-server
```

### To reset the database

Open a new terminal window and activate virtual environment after checking the command:

```
pdm venv activate
```

Then:

```
pdm run init-db
```
