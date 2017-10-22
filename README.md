# Jenkins with Maven Image

Based on [jenkins/jenkins](https://hub.docker.com/r/jenkins/jenkins/)

# Usage
```
docker run -d -p 18080:8080 -p 50000:50000 kemixkoo/jenkins-maven
```
Then, can access Jenkins via http://localhost:18080

In first time, need unlock Jenkins, enable to find the generated password via:
```
docker logs <running-container-id>
```

# Custom Maven Home
```
docker run -d -p 18080:8080 -p 50000:50000 -v /path/to/maven:/opt/maven kemixkoo/jenkins-maven
```

# Custom Jenkins Home
```
docker run -d -p 18080:8080 -p 50000:50000 -v /path/to/jenkins_home:/var/jenkins_home kemixkoo/jenkins-maven
```

# Building
```
docker build -t kemixkoo/jenkins-maven .
```
