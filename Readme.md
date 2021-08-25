# Serve cosimus locally with zola docker container

    docker run -v $(pwd):/app -w /app -p 1111:1111 -p 1024:1024 \
      -u "$(id -u):$(id -g)" balthek/zola:0.14.0 serve \
      --interface 0.0.0.0 \
      --port 1111 \
      --base-url localhost

# Publish

    git push
