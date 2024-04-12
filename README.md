# Valkey.io website

This repo contains the source for the valkey.io website. The temporary staging website can be accessed using https://d18m7x5q574jh8.cloudfront.net.

## Contributing

We welcome contributions! Please see our [CONTRIBUTING](CONTRIBUTING.md) page to learn more about how to contribute to the website.

## Security

If you discover potential security issues, see the reporting instructions on our [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) page for more information.

## License
This project is licensed under the BSD-3-Clause License.

## Build Locally

1. Go to the root of the repo
2. Install [Ruby](https://www.ruby-lang.org/en/) and [RVM](https://rvm.io/)
3. Install [Jekyll](https://jekyllrb.com/)
4. Install dependencies: `bundle install`
5. Build: `bundle exec jekyll serve` for the local server, `bundle exec jekyll build` for one off builds. Either way, the HTML of the site is generated to `/_site`
6. Point your browser at `http://127.0.0.1:4000/`

## Build with Docker

1. `docker buildx build -t valkey.io .`
1. `docker run --volume="$PWD:/srv:Z" --workdir=/srv -p 3000:4000 valkey.io:latest`
1. Open browser to `http://localhost:3000/`