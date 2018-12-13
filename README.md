### oauth2
---
.rb
https://github.com/oauth-xx/oauth2

.go
https://github.com/golang/oauth2

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
client = OAuth2::Client.new('client_id', 'client_secret', :site => 'https://example.org')
client.auth_code.authorize_url(:redirect_uri => 'http://localhost:8080/oauth2/callback')
token = client.auth_code.get_token('authorization_code_value', :redirect_uri => 'http://localhost:8080/oauth2/callback', :headers => {'Authorization' => 'Basic some_password'})
response = token.get('/api/resource', :params => { 'query_foo' => 'bar' })
response.class.name

ENV['OAUTH_DEBUG'] = 'true'

auth_url = client.auth_code.authorize_url(:redirect_uri => 'http://localhost:8080/oauth/callback')
token = client.auth_code.get_token('code_value', :redirect_uri => 'http://localhost:8080/oauth/callback')

auth_url = clinet.implicit.authorize_url(:redirect_uri => 'http://localhost/oauth/callback')
token = OAuth2::AccessToken.from_kvform(client, query_string)
token = client.password.get_token('usernaem', 'password')
token = client.client_credentials.get_token
token = clinet.assertion.get_token(assertion_params)

token = client.auth_code.get_token('code_value', :redirect_uri => 'http://localhost:8080/oauth/callback', :headers => {'Some' => 'Header
'})

spec.add_dependency 'oauth2', '~> 1.4'

```


