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

3. Back to the root project directory `$ cd ..` and run the project using the command:
```sh

$ docker-compose up -d
```