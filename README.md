<h1 align="center">Laravel Backend/API</h1>

## Installation
1. Clone your repository, example:
`git clone https://github.com/wpaphk/card-game`

2. Change directory into the Laravel project.
`cd card-game/backend/`

3. Install all required dependencies.
```
  docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v $(pwd):/var/www/html \
    -w /var/www/html \
    laravelsail/php81-composer:latest \
    composer install --ignore-platform-reqs
```
    
    
NOTE: This may take a while if this is the first time installing this as a container.

4. Set the proper permissions to the project files.
- `sudo chown -R $USER: .`

5. Copy .env File
- `cp .env.example .env`

6. Run the servers with Sail
- `./vendor/bin/sail up -d`

7. Generate APP_KEY Key.
- `./vendor/bin/sail artisan key:generate`

8. Build the seed.
- `./vendor/bin/sail artisan migrate:fresh --seed`

9. npm Install
- `./vendor/bin/sail npm install`

10. npm build
- `./vendor/bin/sail npm run build`

11. You can now open your application with your browser: http://localhost

```
Login
User: admin@example.com
Password: password
```

<h1 align="center">Angular App</h1>

## Installation
1. Change directory into the angular project.
`cd ../high-low-card/`

2. Build the image and fire up the container:
`docker-compose up -d --build`

3. You can now open your application with your browser: http://localhost:4201
