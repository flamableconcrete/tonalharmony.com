# Viewing the Tonal Harmony Website Locally

To run the website locally using Docker, open a terminal in the root of the repository and execute:

docker run --rm -it \
  -p 4000:4000 \
  -v "$(pwd):/srv/jekyll" \
  -v "$(pwd)/vendor/bundle:/usr/local/bundle" \
  jekyll/jekyll:4.2.0 \
  jekyll serve --watch --host 0.0.0.0 --livereload

Once the server starts, open your browser and go to:

<http://localhost:4000>

Notes:

- Make sure Docker is installed and running.
- Your local gems will be cached in the 'vendor/bundle' directory for faster subsequent runs.
- The site will automatically reload when you modify files.
