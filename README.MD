## What I built

Docker Project that containerizes and runs a python app to host a simple webpage using flask.

# Next steps
- Learn how to use flask to host more complex web pages instead of simple text 
- Host the flask container on an AWS EC2 instead of locally 
- Explore how all of this can be automated with a CI/CD pipeline such as Azure DevOps

# Tech Requirements

Docker,Python,Flask 

# What I learned

## Flask 

- Flask depenency in python can be used to host webapps 
- @app.route('/') makes the webapp created the landing/home page on the host
- Networking principle 0.0.0.0 as a host opens it to be accessed by any network/ip


## Docker

- Port mapping as a concept in docker is when you set ports on your machine to ports in your container ; these dont have to be the same eg 8080:5001 
- Requirements.txt file can be used to store dependencies so you can run them as one batch in docker

## Key Commands 

- Docker run -p 5001:5001 docker-flask-app = Runs my app and maps port 5001 on my machine to port 5001 within the container 

- pip3 install flask - installs the dependency flask 


# Errors I faced

- Error : Container would not build due to line in code that installs dependencies 'RUN PIP install requirements.txt'

    ### Troubleshooting : 

    - removed this line and tested to see if instead just adding a line to install the dependency flask worked, it did.
        - ran pip in my terminal and it returned an error but pip3 worked, leading me to believe thats where the issue lied.

     -Fix : Changed code to reflect this and everything was functional again 


- Error : port 5000 was in use on my mac for airplay so couldnt be used to host the webpage 

- FIX : changed to port 5001 which wasnt in use therefore worked




