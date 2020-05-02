# Jenkins 101

## Run Jenkins

```bash
docker run -d -p 8081:8080 --name jenkins1 jenkins/jenkins:lts
```

```bash
docker logs jenkins1
```

Copy the initial admin password from the console logs to paste it when prompted

Browse to <http://localhost:8081> & sign in

## Finish the Jenkins setup

Click _Select plugins to install_ (not _Install suggested plugins_), then:

- select _None_
- finish install & login

## See what we can do

- Left nav has _New Item_, _People_ etc.

- Click _New Item_ to create a job

- Only one type of project, Freestyle

- _Source Code Management_ : none

- _Build Triggers_ : schedule and based on other jobs

- _Build_ : add step, execute shell (Linux only)

- add shell step:

```bash
echo "Hello from build $BUILD_TAG"
```

- click _Build Now_, check build output
