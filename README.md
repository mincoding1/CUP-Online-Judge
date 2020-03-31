# CUP-Online-Judge-NG-Docker-Judger

## Requirements
Install [Docker](https://get.docker.com/) and [Docker Compose](https://docs.docker.com/compose/install/)

## Usage
1. Clone repo inside your project
```bash
git clone https://github.com/ryanlee2014/CUP-Online-Judge-NG-Docker-Judger.git docker-judger
```

2. Enter the folder and rename .env.example to .env, docker-compose.example.yml to docker-compose.yml
```bash
cd docker-judger
cp .env.example .env
cp docker-compose.example.xml docker.compose.yml
```

3. Edit judger/etc/judge.conf and compile.json to your environment settings
```text
# judge.conf
OJ_HOST_NAME=your_mysql_hostname
OJ_USER_NAME=your_mysql_username
OJ_PASSWORD=your_mysql_password
```

4. Make `data` foler and move files into the folder or link `data` folder to `judge/data`
```bash
# make dir
mkdir -p ./judger/data
# link
ln -s path/to/data ./judger/data
```

5. Run your containers:
```bash
docker-compose up -d
```