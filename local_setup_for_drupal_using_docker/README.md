# Local Drupal development using Docker
A basic docker environment to create drupal 8 sites locally.

```
# build docker stack
docker-compose -f local.yml up --build -d

# install drupal inside /code
docker-compose -f local.yml run php composer install

# run drush
docker-compose -f local.yml run php ./vendor/bin/drush --root=/code/web pm-list

# stop 
docker-compose -f local.yml down
```
Errors, and how to fix them: <br>
![2 errors](https://i.imgur.com/TfKjHTh.png)

Sources:
* [shapeblock](https://www.shapeblock.com/local-drupal-development-using-docker/)