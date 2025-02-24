#### Create telegram bot

- Access telegram, find bot: @BotFather
- Type: "/newbot"
- Type your bot name: "username_bot"
- Create group add add "username_bot" to group (bot is admin)
- Save the telegram token

#### Create OpenAI API key

Go to https://platform.openai.com/api-keys to create API key

#### Add open_ai_key and telegram_bot

`EDITOR='code . --wait' rails credentials:edit` to add open_ai_key, telegram_bot
`EDITOR=nano rails credentials:edit --environment development        `

#### Install gems

```ruby
gem 'telegram-bot-ruby', '2.4.0'
gem 'ruby-openai'
gem 'sidekiq'
# gem 'faraday', '2.12.2'
# gem 'json', '2.10.1'

gem install telegram-bot-ruby -v '2.4.0'
gem install faraday -v '2.12.2'
gem install json -v '2.10.1'
gem install ruby-openai
```

#### Get id

Go to https://api.telegram.org/bot{telegram_bot_token}/getUpdates

#### Create some files

```ruby
# /home/nguyenloi/Desktop/telegram_ai/config/initializers/telegram_bot.rb

# /home/nguyenloi/Desktop/telegram_ai/Procfile.dev

# /home/nguyenloi/Desktop/telegram_ai/app/workers/telegram_bot_worker_job.rb

# /home/nguyenloi/Desktop/telegram_ai/app/services/telegram_botter.rb

# /home/nguyenloi/Desktop/telegram_ai/app/models/post.rb

```

#### Test

Create new post at http://127.0.0.1:3000/posts/new
