# Proxy based on query string

This repo serves as an example of how to route traffic, based on a query
parameter.

## Run

Clone this repo, run `docker-compose up -d` and visit either http://localhost
for v1 and http://localhost/?v=2 for v2 of the site.

## Implementation

Once you run the project, three containers will be created. Two are simple
Python servers, each running a different site.

The third container is an Nginx container that runs a custom Nginx config. The
gist of the solution is to use Nginx's `map` directive to set the backend server
to `site1` or `site2`, depending on whether a query parameter of `v` equals to
`2`.

## Watch demo

See the demo [here](https://github.com/rokcarl/proxy-by-query/blob/b19c47ece6d74f18d10efe307d531c087461e5a6/resources/demo/c9pJ18O05l.gif).