# fullcycle-sonarqube
    docker run -d --name sonarqube -e SONAR_ES_BOOTSTRAP_CHECKS_DISABLE=true -p 9000:9000 sonarqube:latest
    docker run -d -p 8084:9000 mwizner/sonarqube:8.7.1-community

# Login initial
    user: admin
    pws: admin or sonarqube

# Create project 
    token a794e730b952d0669410af9f89bc0843cf7cedd4

# Scanner 
sonar-scanner \
  -Dsonar.projectKey=fullcycly-go \
  -Dsonar.sources=. \
  -Dsonar.host.url=http://localhost:8084 \
  -Dsonar.login=a794e730b952d0669410af9f89bc0843cf7cedd4

# Js
    npm install jest @types/jest sonar-scanner --only-dev