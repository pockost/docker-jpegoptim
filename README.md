# Usage

## One file optimization
You have to mount image folder to optimized into /app directory. Example :

```
docker run --rm -v "$( pwd ):/app" pockost/jpegoptim -s -t images.jpg
```

## Get help

If you run the container without any option help will be show.

```
docker run --rm pockost/jpegoptim
```

## Multiple file optimization

You can also pipe the result of a find command

```
docker run --rm -v "$( pwd ):/app" -w /app alpine find -iname '*.jpeg' -o -iname '*.jpg' |  xargs docker run --rm -v "$( pwd ):/app" pockost/jpegoptim --max=90 --strip-all --preserve --totals -v
```

# User feedback

If you have any problems with or questions about this Docker image, please contact us through a Github issue.
