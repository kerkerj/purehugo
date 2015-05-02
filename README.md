purehugo-kerkerj
========

This repo is forked from [dplesca/purehugo](https://github.com/dplesca/purehugo)

## How to use this theme

```
$ cd /to/your/hugo/blog
$ git clone https://github.com/kerkerj/purehugo purehugo-kerkerj
$ hugo server --theme=purehugo-kerkerj
```

## Config file

The config file in toml format:

```toml
baseurl = "http://dplesca.github.io/purehugo/"
languageCode = "en-us"
title = "purehugo"
theme = "purehugo-kerkerj"
Paginate = 10
disqusShortname = "xxxx"

[params]
  twitter: "twitter_id"
  github: "github_id"
  facebook: "facebook_id"
  linkedin: "linkedin_profile_url"  
  description = "Demo site for a hugo theme"
  google_analytics = "UA-xxxxxx-xx"
  highlight_style = "railscasts"
```

The config file in yaml format:

```yaml
baseurl: "http://dplesca.github.io/purehugo/"
languageCode: "en-us"
title: "purehugo"
theme: "purehugo-kerkerj"
Paginate: 10
disqusShortname: "xxxx"

params:
  twitter: "twitter_id"
  github: "github_id"
  facebook: "facebook_id"
  linkedin: "linkedin_profile_url"
  description: "Demo site for a hugo theme"
  google_analytics: "UA-xxxxxx-xx"
  highlight_style: "railscasts"
```

`highlight_style` default value is `solarized_dark`

If you want to change that, here is the [list](https://highlightjs.org/static/demo/)

Notice the configuration necessary for disqus comments (just setting the disqusShortname), the twitter and github handlers (for the site sidebar), the site description and enabling Google Analytics reporting.

## Syntax Highlighting

`purehugo` used [rainbow js](http://craig.is/making/rainbows) library for syntax highlighting.

I changed it to [highlight.js](https://github.com/isagalaev/highlight.js)

The way to use highlighting doesn't change, 

just add language in code block like this:

<pre>
```ruby
def say
	puts "hello"
end
```
```go
func main() {
	fmt.Println("Hello")
}
```
</pre>


## Reponsive Images

For responsive images you could use the built-in responsive image shortcode:  
```
{{%/* img-responsive http://example.com/image.jpg */%}}
```

## Build yourself

`purehugo` use `gulp` to pack the static files.

So, first you need to install `gulp`, which means you need `nodejs` installed.

```
$ cd purehugo-kerkerj
$ npm install
```

This will help you to install:

```
"gulp": "^3.8.11",    
"gulp-concat": "^2.5.2",
"gulp-minify-css": "^1.1.0",
"gulp-uglify": "^1.2.0"
```

Packing static files:

```
$ gulp compress
```

Just edit `gulpfile.js` to add tasks you want.