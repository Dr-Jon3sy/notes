## Project Notes

### SkyDaddy

Honestly the name is already pissing me off, will have to work on that

Learning about apps...by having chatGPT do it all for me. Woot. 

Honestly its a bunch of things that I've done before or know how to do but haven't strung together all in one. Be good to get something running as a service that actually sees the front end. 

#### Images in Readmes
----
Fun fact - ```png``` and ```jpg``` images, because of variations in how transparency (sp) is handled, can differ...mostly by ```png``` images looking blue. Love that. 

60% keyboard I'm using is great until it isn't - specifically backtick and tilde characters are an annoying combination (```FN-ESC``` and ```FN-SHFT-ESC``` respectively). Which is fine...until you're in markdown, or on Linux again and being able to use the alias to home is REALLY FREAKING NICE.  

#### Running things
----
Ok we're runing flask, pretty straightforward

remember the environment variables - can some of these be stored in the .env? need to check if flask can read those automatically

#### FUCKING LOL
----
ok found out why "no one has done this simple thing" - twitter charges 200 a month for access to anything more than reading 100 posts and writing 500 sooooo this is even more academic than we first thought

Annoyingly, twitter auth/sign in and whatever only seems to work in Chrome? Which is typical tbh. 

#### OAUTH 
----
so oauth uses a 3 legged process

1. client (our software) generates a request token by asking google/twitter/whoever for a temp token signed using the clients creds. Temp token is called a request token
1. the client then passes the user off to the provider (twit/goog) where they log in and say "yep this is good". Provider returns a "verifier" via a CALLBACK URL
1. the combination of request token AND access token is passed back to the provider, who returns an access token

#### OAUTH_2.0
----
Less crypto more betterer...right?

1. Client redirect user to auth server - included is client ID, redirect URI and that should be it
1. User logs into provider - redirected back to client with an auth code
1. auth code plus client secret (c r y p t o) is exchanged at an endpoint for an access token which can be user to get bearer s t u f f