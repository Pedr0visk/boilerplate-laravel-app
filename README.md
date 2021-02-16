### Prerequisites
1. Docker

### Installation

1. Clone the repo
```sh

$ git clone git@github.com:Pedr0visk/boilerplate-laravel-app.git
```

2. Next, use *Docker’s composer image* to mount the directories that you will need for your Laravel project and avoid the overhead of installing Composer globally
```sh

$ cd laravel-app && docker run --rm -v $(pwd):/app composer install
```

3. Back to the root project directory `$ cd ..` and modify the environment settings to run the containers:
```sh

$ cp .env.example .env
$ nano .env
```

**replace to:**

```sh
DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=you_laravel_db_user
DB_PASSWORD=your_laravel_db_password
```

after that, run the containers:

```sh

$ docker-compose up -d
```