## PassTy: web application to keep your passwords in one place behind firewall install 

[![Build Status](https://travis-ci.org/randx/passty.png)](https://travis-ci.org/randx/passty)
[![Coverage Status](https://coveralls.io/repos/randx/passty/badge.png)](https://coveralls.io/r/randx/passty)
[![Code Climate](https://codeclimate.com/github/randx/passty.png)](https://codeclimate.com/github/randx/passty)

![screenshot](https://raw.github.com/randx/passty/master/public/screenshot.png)

### Requirements:

* ruby 1.9+
* mysql or postgres db

### Setup:


1. Get code

        git clone https://github.com/randx/passty.git
        cd passty


2. Copy database.yml and edit db user/password


        # MySQL
        cp config/database.yml.mysql config/database.yml
         
        # or Postgres
        cp config/database.yml.postgres config/database.yml

        # or sqlite
        cp config/database.yml.sqlite config/database.yml

        vim config/database.yml


3. Setup libs, migrations etc

        bundle install --deployment --without development test
        bundle exec rake db:create RAILS_ENV=production
        bundle exec rake db:setup RAILS_ENV=production
        bundle exec rake assets:precompile RAILS_ENV=production 

4. Run application on 3000 port
        
        bundle exec rails s -e production -p 3000


- - -

Pull Requests are welcome :)
