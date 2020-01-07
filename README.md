# twitter-cloud-run

A minimal configuration app to run Twitter bots on a schedule using Google Cloud Run and Google Cloud Scheduler, making running the bot effectively free and can scale to effectively an unlimited number of bots if necessary.

There are two variants in their respective folders:

* `human_curated` : Uses a centralized Cloud SQL database to load pregenerated Tweets, and records if a tweet is generated. Recommended for AI tweet generation due to unpredictibility of AI-generated tweets.
* `gpt-2`: Uses an pretrained GPT-2 model, similar to the gpt2-cloud-run repo. (although the base `app.py` is built for `gpt-2-simple`, it's easy to hack it out and replace your own method of text generation for the bot.

## Usage

The app is configured using Environment Variables; this avoids hardcoding the access tokens within the container and therefore a security risk (encoding secrets in environment variables isn't the *ideal* solution for handling secrets in general, but it is sufficient for this app)

Additionally, you can specify a `REQUEST_TOKEN` as an Environment Variable, to prevent others from triggering the app accidentially (i.e. via random IP sniffing, as Cloud Run URLs are public).

See the READMEs in the folders for more pertinent information to the app.

## Helpful Notes

## Maintainer/Creator

Max Woolf ([@minimaxir](https://minimaxir.com))

*Max's open-source projects are supported by his [Patreon](https://www.patreon.com/minimaxir) and [GitHub Sponsors](https://github.com/sponsors/minimaxir). If you found this project helpful, any monetary contributions to the Patreon are appreciated and will be put to good creative use.*

## License

MIT

## Disclaimer

This repo has no affiliation with Twitter Inc.