# Twitter_realtime_acquisition
Acquisition of Real time tweets based on climate change using twitter streaming API and Hashtags
Steps to run the application:

1.) Download docker from https://www.docker.com/products/docker-desktop for your operating system.

2.) Create a working directory and copy the following files in to the directory.

a) dockerfile
b) tweet_processor.py
c) tweet_streamer.py

3.) Open terminal and run the following commands(cd working directory) from inside the directory created in step 2.
    
    docker build -t project/tweeter-streamer .       <-  Note "." is included in the command.

    Replace the path /home/abhinav/Project in the following command with a directory on your 
    operating system where the output file will be written.
    
    docker run -it --name twitter_streaming_app --restart=always -v /home/abhinav/Project:/home/tweet project/tweeter-streamer:latest
    
    Check the running container with the following command:
    
    docker ps
    
    Use the following commands to start and stop the script.
    
    (Container id is obtained by running the docker ps command)
    
    docker start <container id>       
    docker stop <container id>
