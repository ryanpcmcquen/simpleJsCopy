# simpleJsCopy :clipboard:

Just include the library (`v0.3.1`, ~1kB!):

    <script src="https://cdn.rawgit.com/ryanpcmcquen/simpleJsCopy/7a5a88c0a43eaa95c03146555a45428407735d56/simpleJsCopy.min.js"></script>

https://cdn.rawgit.com/ryanpcmcquen/simpleJsCopy/7a5a88c0a43eaa95c03146555a45428407735d56/simpleJsCopy.min.js

Then use the following elements:

1. `<textarea>` with the class `text-to-copy` (can be `readonly` but *not* `disabled`)
2. `<button>` with the class `js-copy-btn`

The library takes cares of the rest. :shipit:

:newspaper: You don't have to write any JavaScript to use it!

=====

#### So what?! Where does it work?

Almost everywhere!

Desktop:

- Chrome/Chromium 42+
- Firefox 41+
- Internet Explorer 9+
- Opera 29+
- Safari 10+

Android:

- Chrome 42+
- Firefox 41+

iOS:

- 10+

##### What about other browsers?

Everywhere else (old versions of Safari), it will select the text. The library detects iDevices and will change the inital button text to `Select text` (to avoid confusing the user). After clicking it will say either `Now tap 'Copy'` (iPhone) or `Now tap the text, then 'Copy'` (iPad), to account for the strange behavioral differences of these devices.

On desktop Safari (< v10), the button will change to `Press Command + C to copy`.

On failure the button will say `Please copy manually`.

=====

:warning: If you want your textarea to be invisible for some reason, use this CSS:

```css
.text-to-copy {
  opacity: 0;
  position: absolute;
}
```

Because it will not work with `display: none;` or `visibility: hidden;`. :thumbsup:

Note that you should also supplement that CSS with something like this helper library, otherwise people on iOS will not be able to copy at all since Safari doesn't support cool stuff:

https://gist.github.com/ryanpcmcquen/1229119ffcf5098543c0

#### What else is cool?

If you aren't concerned with maximum compatibility, you can use elements besides a `textarea`. In the next version you will be allowed to add multiple copy elements to a page.
