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

## Training Guide
https://laravel.com/docs/5.1/quickstart


### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
