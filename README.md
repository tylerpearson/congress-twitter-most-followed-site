# Jekyll site to display results from [Twitter Most Followed](http://github.com/tylerpearson/twitter-most-followed-scripts)

This is a Jekyll site to display the results generate by the scripts in the [Twitter Most Followed repo](http://github.com/tylerpearson/twitter-most-followed-scripts) for Congress.

## Setup

### Development

Run the site locally with `jekyll build --watch`.

### Production

Since the site is static, it can be [served over S3](http://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteHosting.html). I've found that the easiest way to upload the site is with [s3cmd](https://github.com/s3tools/s3cmd) and simplify caching with (Cloudflare)[https://cloudflare.com]. A sample command is `s3cmd sync _site/ s3://congress-on-twitter.tylerp.me` adjusted to your bucket name.

If SSL is important, [use Cloudfront](http://www.michaelgallego.fr/blog/2013/08/27/static-website-on-s3-cloudfront-and-route-53-the-right-way/) because https with Cloudflare won't currently work with serving a website through S3.

## License

MIT
