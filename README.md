# Weatherbooot

App created during workshop on the Elixir Live conference(based on the [fork](https://github.com/pferdefleisch/Elixir-wit.ai-Facebook-starter-bot.git))
It's an umbrella app which contains web interface as a phoenix app (apps/web_api) and bot utils(apps/bot).

## Development env setup

* fetch dependecies using `mix deps.get`
* copy `.env.example` to `.env`
* set [`WitAI`](https://wit.ai/aokon) api key in your `.env`
* create [account](https://openweathermap.org) and set WEATHER_API_KEY
* set random hash for the FACEBOOK_CHALLENGE
* create a new [`Messanger app`](https://developers.facebook.com/), in your webhooks configuration set `messages, messaging_postbacks` options
* create a new Facebook fan page where your bot will be working
* Add your `FACEBOOK_CHALLENGE` token to `Generate token` section of the messanger app config and select fan page where your app will be working.
* create secure connection for your local app using [`ngrok`](https://ngrok.com) e.g `./ngrok http 4000`
* set secure url from ngrok and add verification to your messanger app
* export your env setting before run your web api using `source .env`
* run web api `mix phoenix.server`

## WitAI

Create stories for your bot which will be respond to bot weather actions. I recommend to check some [`tutorials`](https://wit.ai/docs/quickstart) on the WitAI page to be more familiar with the app features.
