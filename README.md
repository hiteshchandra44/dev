# dev


program 1,2:

git config --global user.name kiranmr2024
git config --global user.email kiranmr2024@gmail.com
touch file.txt
echo "Hi">file.txt
git init
git add file.txt
git commit -m "Initial"
git remote add origin https://github.com/kiranmr2024/test106.git
git branch -M main
git push origin main
git checkout -b sample
touch second.txt
echo "Hello">second.txt
git add second.txt
git commit -m "Second"
git push origin sample
git checkout main
git merge sample
git push origin main

prog 3 addition file:

def add(a,b):
    return a+b
def test_add():
    assert add(1,2) == 3
    assert add(2,2) == 4

program 3 yaml file:


name: First GitHub Actions # Name of the GitHub Actions workflow.

on: [push] # Trigger this workflow on push events.

jobs:
  build: # Job name.
    runs-on: ubuntu-latest # The job runs on the latest version of Ubuntu.

    strategy:
      matrix:
        python-version: [3.8, 3.9] # The job runs on Python versions 3.8 and 3.9.

    steps:
      # Step 1: Check out the repository code into the runner.
      - uses: actions/checkout@v2

      # Step 2: Set up the specified Python version from the matrix.
      - name: Setting up Python
        uses: actions/setup-python@v2
        with:
          python-version: ${{ matrix.python-version }}

      # Step 3: Install all the dependencies required for the tests.
      - name: Installing all the dependencies
        run: |
          python -m pip install --upgrade pip # Upgrade pip.
          pip install pytest

      # Step 4: Run the tests using pytest.
      - name: Running tests
        run: |
          python -m pytest addition.py

prog 3 commands:

cd ..
cd ..
cd ..
cd d
cd dev
git init
git status
git add .
git commit -m "Initial"
git branch -M main
git remote add origin https://github.com/kiranmr2024/dev3.git
git push -u origin main
mkdir actions-runner
cd actions-runner
curl -L -o actions-runner-win-x64-2.321.0.zip https://github.com/actions/runner/releases/download/v2.321.0/actions-runner-win-x64-2.321.0.zip 
unzip actions-runner-win-x64-2.321.0.zip
./config.cmd --url https://github.com/kiranmr2024/dev3 --token BNC5FIDPQM72IPCPNAMK2GTHLPTXU

prog 4 commands:

docker-machine create default --virtualbox-no-vtx-check

docker version
docker ps
docker run hello-world
docker run busybox
docker run --privileged redis
docker ps
docker exec -i -t [id] sh
>>cd ../
>>ls

prog 5 commands:

DockerFile:

FROM alpine

RUN apk add --update redis

CMD ["redis-server"]

commands in terminal:

docker build .
docker run [docker_id]
docker build -t hitesh/redis:latest .
docker run hitesh/redis

prog 6 commamds:

sonar.projectName=lab6
sonar.projectKey=lab6
sonar.projectVersion=1.0
sonar.language=java
sonar.sources=src/main/java
sonar.tests=src/test/java
