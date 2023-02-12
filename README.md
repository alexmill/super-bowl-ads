
# Super Bowl ads CPM pricing over time


# Getting Started: 

- `docker`
0. Install Docker for your system.
1. Install `git` and clone this repo.
2. Navigate into the repo and "Build" the container for this project. This downloads all the pre-requisite software to run this container.
```bash
cd ./<this dir> 
docker build -t superbowl .
```
3. Get the `$IMAGE_ID` of the Docker image you just created:
```bash
IMAGE_ID=$(docker image ls | grep superbowl | awk '{print $3}')
```
4. "Run" the generated Docker image and launch Jupyter with the following command:
```bash
docker run \
  --volume $(pwd):/home/jovyan \
  --publish 8887:8888 \
  --network host\
    $IMAGE_ID
```
- Roll your own: If your system has `pandas`, `lxml`, and `matplotlib` installed, you should be able to execute the notebook. 



