web: rails server -p $PORT -e $RAILS_ENV

RACK_ENV=none RAILS_ENV=development unicorn -c config/unicorn.rb

web: bundle exec unicorn -p $PORT -c ./config/unicorn.rb

worker: bundle exec sidekiq --environment development -C config/sidekiq.yml

tail: -f log/development.log