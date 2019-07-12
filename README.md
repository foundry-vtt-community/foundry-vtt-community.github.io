# Foundry Community Website

Go to [the website](https://aksakalli.github.io/jekyll-doc-theme/) for more detailed information.

## Running Locally

You need Ruby and gem before starting, then:

```bash
# Install bundler
gem install bundler

# Clone the project
git clone https://github.com/foundry-vtt-community/foundry-vtt-community.github.io.git
cd foundry-vtt-community.github.io

# Run Jekyll with dependencies
bundle exec jekyll serve
```

## Docker

Alternatively, you can deploy it using the multi-stage [Dockerfile](Dockerfile)
that serves files from Nginx for better performance in production.

Build the image for your site's `JEKYLL_BASEURL`:

```
docker build --build-arg JEKYLL_BASEURL="/your-base/url" -t foundry-vtt-community.github.io .
```

(or leave it empty for root: `JEKYLL_BASEURL=""`) and serve it:

```
docker run -p 8080:80 foundry-vtt-community.github.io
```

## License

Released under [the MIT license](LICENSE).
