# Basic setup docker with nodejs app

## I. Set up docker environment

### Set up the repository

#### 1. Update the `apt` package index and install packages to allow `apt` to use a repository over HTTPS:

```bash
$ sudo apt-get update

$ sudo apt-get install \
  ca-certificates \
  curl \
  gnupg \
  lsb-release
```

#### 2. Add Docker’s official GPG key:

```bash
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

#### 3. Use the following command to set up the stable repository. To add the **nightly** or **test** repository, add the word **nightly** or test (or both) after the word **stable** in the commands below.

```bash
  $ echo \
    "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
    $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

### Install Docker Engine

#### 1. Update the `apt` package index

```bash
  $ sudo apt-get update
```

#### 2. Install the _latest_ version of Docker Engine and containerd

```bash
  $ sudo sudo apt-get install docker-ce docker-ce-cli containerd.io
```

## II. Set up docker environment

#### 1. Create a image from docker file

```bash
  $ docker build -t your-node-app:your_tag
```

#### 2. Run image to create container

```bash
  $ docker run -p 5001:8080 your-node-app:your_tag
```

#### 3. Visit your app at [http://localhost:5001](http://localhost:5001/)

<div align="center">
    <img src="/course-service/public/images/node_app_running.png">
</div>

#### 4. Run multiple container to interact with other by using `docker-compose`

```bash
  $ docker-compose up -d
```

#### 5. Visit your app at [http://localhost:5002](http://localhost:5002/)

<div align="center">
    <img src="/course-service/public/images/web_app.png">
</div>
