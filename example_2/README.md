# Docker FastAPI example #

This example containerises a dummy FastAPI python app

### Requirements.txt ###
We've installed `fastapi` and `uvicorn` manually in the venv via `pip3`.\
Then we generated the `requirements.txt` file by running `pip3 freeze > requirements.txt` \

### Dockerfile notes ###
In the `Dockerfile` the `RUN` line uses the `--no-cache-dir`.  This makes subsequent Docker builds much faster as it uses the docker cache not the pip cache\
We also use the `requirements.txt` file and `--upgrade` flag ensures we keep up to date with the `requirements.txt` file.\
We also need to specify a bunch of parameters to `uvicorn` to map the URL and host.\

### Docker build ###
`docker build -t fastapi-tutorial .`

### Docker run ###
`docker run -d --name myfastapicontainer -p 80:80 fastapi-tutorial`

### In the browser ###
Hello World page should appear when browsing to http://0.0.0.0:80\
Test the `items` endpoint with http://0.0.0.0/items/123?q=hello\
JSON response should be `{"item_id":123,"q":"hello"}`\





