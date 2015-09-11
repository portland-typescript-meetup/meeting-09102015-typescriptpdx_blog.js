# This repo was created for a presentation at the Portland TypeScript Meetup on September 10, 2015
Andrew's [Slide Deck](http://cl.ly/401Q053E2T3Q) is eye-opening and inspiring.

# typescriptpdx_blog

A simple module that gets the latest metadata from the blog posts on the TypeScriptPDX blog

## Basic Usage

```javascript
var Blog = require("typescriptpdx_blog");

var pdxBlog = new Blog();

/**
* When the "end" event is triggered an array of article 
* metadata is returned
**/
pdxBlog.on("end", console.dir);

/**
* If a parsing, network or HTTP error occurs an
* error object is passed in to the handler or callback
**/
pdxBlog.on("error", console.error);
```

### Example of Returned Data

```javascript
[
    {
        title: 'WebStorm and TypeScript',
        link: 'http: //typescriptpdx.com/blog/2015/07/webstorm-and-typescript',
        publishDate: new Date("Sat Jul 25 2015 17:00:00 GMT-0700 (PDT)")
    },
    {
        title: 'TypeScript - A Brief Overview',
        link: 'http: //typescriptpdx.com/blog/2015/07/typescript-a-brief-overview',
        publishDate: new Date("Sun Jul 12 2015 17:00:00 GMT-0700 (PDT)")
    }
]
```

`title` and `link` are `string`s and `publishData` is a JavaScript `Date` object.
