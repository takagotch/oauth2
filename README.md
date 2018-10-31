### oauth2
---
https://github.com/oauth-xx/oauth2

```ruby
client = OAuth2:Client.new(key, secret,
  :site => site, :authorize_url => auth_url, :token_url => token_url) do |b|
  b.request :multipart
  b.request :url_encoded
  b.adapter :net_http
end

begin
  img = Faraday::UploadIO.new('play.gif', 'image/gif')
  data = {:content => "this is a tile", :img => img}
  response = token.post('api/v1/tiles/', :body => data)
  print response.body, response.status
resuce OAuth2::Error => e
  puts e
end

```

```
git clone git@github.com:oauth-xx/oauth2.git
bundle install
bundle exec rake

gem 'oauth2'
bundle 
gem install oauth2


```

```ruby
require 'oauth2'
client = OAuth2::Client.new()
client.auth_code.authorize_url()
token = client.auth_code.get_token()
response = token.get()
response.class.name


```


