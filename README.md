# Foundry Community Website

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

## Themes Used

### Jekyll Theme

Go to [jekyll doc theme's website](https://github.com/aksakalli/jekyll-doc-theme) for more detailed information about the Jekyll theme.

### Bootstrap Theme

Go to [the superhero theme](https://bootswatch.com/superhero/) for more detailed information about the Bootstrap theme.

## License

Released under [the MIT license](LICENSE).
