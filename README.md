# Usage

## Install bundle dependencies

```` sh
docker run --rm -ti \
    --workdir '/code' \
    -v "${PWD}:/code" \
    -v "${PWD}/.gems:/usr/local/bundle" \
    -p "4000:4000" \
    mathieubrun/jekyll:latest install
`````

## Run with default parameters

```` sh
docker run --rm -ti \
    --workdir '/code' \
    -v "${PWD}:/code" \
    -v "${PWD}/.gems:/usr/local/bundle" \
    -p "4000:4000" \
    mathieubrun/jekyll:latest
````

## Run with custom parameters (for example --incremental)

```` sh
docker run --rm -ti \
    --workdir '/code' \
    -v "${PWD}:/code" \
    -v "${PWD}/.gems:/usr/local/bundle" \
    -p "4000:4000" \
    mathieubrun/jekyll:latest exec jekyll serve -H 0.0.0.0 --incremental
````