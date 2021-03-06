# JoindIn.js #

[JoindIn.js](https://github.com/AurelioDeRosa/JoindIn.js) is an unofficial JavaScript library to embed Joind.in
comments, talks, and more. The library is written in plain JavaScript, so has no dependencies.

## Compatibility ##

JoindIn.js has been tested on the following browsers: Internet Explorer 9+, Chrome, Opera, Firefox, and Safari.

## Demo ##
A live demo is available [here](http://htmlpreview.github.io/?https://github.com/AurelioDeRosa/JoindIn.js/blob/master/demo/index.html).

## Elements supported ##

The library supports the following elements:

* Talk (`data-type="talks"`)
* Comment (`data-type="talk_comments"`)

More elements will be integrated soon.

## Installation ##

You can install JoindIn.js using [Bower](http://bower.io):

```shell
bower install joindin-js
```

Then, include the JavaScript file in your web page as shown below:

```html
<script src="bower_components/joindin-js/dist/joindin.min.js" async></script>
```

**Note**: the `async` attribute isn't necessary but can improve the performance of your website.

If you don't have or don't want to use Bower, you can clone this repository running the command:

```shell
git clone https://github.com/AurelioDeRosa/JoindIn.js.git
```

The last option is to manually download the library.

## Usage ##

Once you have the JavaScript file in place, you have to create one or more DOM elements for every element you want to
embed: talk, comment, or any other of the [element supported](#elements-supported). The DOM elements you create must
use the class `joindin-embed` and define two `data-*` attributes:

* `data-id`: the ID of the element you want to embed. To know how to retrieve the ID of an element read the
section [How to retrieve the ID of the element to embed](#how-to-retrieve-the-id-of-the-element-to-embed);
* `data-type`: [the type of the element](#elements-supported) to embed.

### Embedding a talk ###
To embed my talk "[Modern front-end with the eyes of a PHP developer](https://joind.in/talk/view/10889)",
you have to add the following element to your page:

```html
<div class="joindin-embed" data-id="10889" data-type="talks">
</div>
```

### Embedding a comment on a talk ###

To embed one specific comment published on the same talk, you have to add the following element instead:

```html
<div class="joindin-embed" data-id="44197" data-type="talk_comments">
</div>
```

Note that in this case the ID refers to the comment, not the talk.

### How to retrieve the ID of the element to embed ##

Retrieving the ID of the element you want to embed is the tricky part of using this library.

For a talk the ID can be found in the URL of the website. For example, the URL of my talk
"[Modern front-end with the eyes of a PHP developer](https://joind.in/talk/view/10889)" is
[https://joind.in/talk/view/10889](https://joind.in/talk/view/10889), so its ID is 10889.

To retrieve the ID of a comment you have to look at the source code of the page. It's written as part of the class
name set to the element wrapping each comment. For example, you can find a class name like `comment-43964` where
43964 is the ID of the comment.

## Note ##

JoindIn.js is in a very early stage, so it's not stable and [every contribution is welcomed](#contribute).

## Contribute ##

I'd love the contribution of anyone who is keen to help. Report a bug, fix a issue, suggest a feature:
any contribution to improve the project is highly appreciated. If you're uncertain whether an addition should be
made, feel free to open up an issue so we can discuss it.

## License ##

JoindIn.js is dual licensed under [MIT](http://www.opensource.org/licenses/MIT) and
[GPL-3.0](http://opensource.org/licenses/GPL-3.0)

## Author ##

[Aurelio De Rosa](http://www.audero.it) ([@AurelioDeRosa](https://twitter.com/AurelioDeRosa))