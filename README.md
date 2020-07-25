## Welcome to Laravel Training

You can use view the presentation slides on [Laravel Training - 0720](https://docs.google.com/presentation/d/e/2PACX-1vS6ybQVVW6tsZLg2OZgeYAAlgmQ65CX3bLAu0DzcvNLC34NyAwA11ajjwYrTXN3g_rqQblMBlhczLfe/pub?start=false&loop=false&delayms=3000) to follow and preview the content for the training.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.


## Installing Laravel on Ubuntu
```bash
sudo apt update -y
sudo apt install openssl php-common php-curl php-json php-mbstring php-mysql php-xml php-zip
sudo apt install composer -y
composer global require laravel/installer
```

> Check if the Laravel is installed by executing the following command:
> ```bash
> laravel
> ```
> 
> If it returns, `laravel: command not found`, then you will need to run the following command:
> ```bash
> echo 'export PATH="$PATH:$HOME/.config/composer/vendor/bin"' >> ~/.bashrc
> bash
> ```

```
git clone https://github.com/JamaicanDevelopers/Laravel-QuickStart-Task-List.git laravelqslt
```

```
cd laravelqslt
sudo apt install -y docker-compose
sudo service mysql stop
```

Create a file called `docker-compose.yml` and add this content.
```
version: '3.3'

services:
    db:
        image: mysql:5.7
        # volumes:
        #     - db_data:/var/lib/mysql
        restart: always
        environment:
            MYSQL_ROOT_PASSWORD: somewordpress
            MYSQL_DATABASE: laravel
            MYSQL_USER: laravel
            MYSQL_PASSWORD: laravel
        network_mode: "host"
```

Create a .env file and add the following content
```php
APP_NAME=Laravel
APP_ENV=local
APP_KEY=
APP_DEBUG=true
APP_URL=http://localhost

LOG_CHANNEL=stack

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=

BROADCAST_DRIVER=log
CACHE_DRIVER=file
QUEUE_CONNECTION=sync
SESSION_DRIVER=file
SESSION_LIFETIME=120

REDIS_HOST=127.0.0.1
REDIS_PASSWORD=null
REDIS_PORT=6379

MAIL_MAILER=smtp
MAIL_HOST=smtp.mailtrap.io
MAIL_PORT=2525
MAIL_USERNAME=null
MAIL_PASSWORD=null
MAIL_ENCRYPTION=null
MAIL_FROM_ADDRESS=null
MAIL_FROM_NAME="${APP_NAME}"

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_DEFAULT_REGION=us-east-1
AWS_BUCKET=

PUSHER_APP_ID=
PUSHER_APP_KEY=
PUSHER_APP_SECRET=
PUSHER_APP_CLUSTER=mt1

MIX_PUSHER_APP_KEY="${PUSHER_APP_KEY}"
MIX_PUSHER_APP_CLUSTER="${PUSHER_APP_CLUSTER}"
```

```
docker-compose up -d
php artisan serve --host 0.0.0.0 --port 8080
```


## Training Guide
https://laravel.com/docs/5.1/quickstart


### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
