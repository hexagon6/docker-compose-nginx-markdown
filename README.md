# docker compose nginx markdown

This repo provides a docker compose setup for running nginx with a markdown converter called [ngx_markdown_filter_module](https://github.com/ukarim/ngx_markdown_filter_module.git).

## usage

1. clone this repo
2. run `docker compose build`
3. run `docker compose up`
4. go to [http://localhost/](http://localhost/) to see test pages rendered as html. they can be found in `public/` of this repo

## features / non-features

- nginx is compiled without ssl, intended to be used behind a tls-terminated reverse proxy
- markdown (with github flavored markdown syntax) files with .md extension are converted to html with `ngx_markdown_filter_module`.

## running in production

1. modify the volume location inside compose.yml
2. run `docker compose up -d`
3. add .md files to your volume for pages
