# Basic setup docker with nodejs app

<!--Create a image from docker file -->

<!-- docker build -t my-node-app:v0.0.1 -->

## Set up docker environment

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

      #### 3. Use the following command to set up the stable repository. To add the **nightly** or **test** repository, add the word      **nightly** or test (or both) after the word **stable** in the commands below.

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

      #### 2. Install the *latest* version of Docker Engine and containerd

      ```bash
        $ sudo sudo apt-get install docker-ce docker-ce-cli containerd.io
      ```

<!-- Run image -->

<!-- sudo docker run -p 5001:8080 my-node-app:v0.0.1 -->
