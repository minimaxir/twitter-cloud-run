# twitter-cloud-run

A minimum configuration tool to run Twitter bots on a schedule using Google Cloud Run and Google Cloud Scheduler, making running the bot effectively free.

## Usage

The app is configured using Environment Variables; this avoids hardcoding the access tokens within the container and therefore a security risk (encoding secrets in environment variables isn't the *ideal* solution for handling secrets in general, but it is sufficient for this app)

Additionally, you can specify a `REQUEST_TOKEN` as an Environment Variable, to prevent others from triggering the app accidentially (i.e. via random IP sniffing, as Cloud Run URLs are public).

## Helpful Notes

## Maintainer/Creator

Max Woolf ([@minimaxir](https://minimaxir.com))

*Max's open-source projects are supported by his [Patreon](https://www.patreon.com/minimaxir) and [GitHub Sponsors](https://github.com/sponsors/minimaxir). If you found this project helpful, any monetary contributions to the Patreon are appreciated and will be put to good creative use.*

## License

MIT
