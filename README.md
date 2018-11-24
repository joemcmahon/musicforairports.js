# Music for Airports

A JavaScript edition of [Ambient 1: Music for Airports 2/1](https://en.wikipedia.org/wiki/Ambient_1:_Music_for_Airports)
by Brian Eno, as built in the [JavaScript Systems Music](http://teropa.info/blog/2016/07/28/javascript-systems-music.html) guide.

This is a new composition, using the base code from Tero's original, and adding some
features to get the result I was looking for.

 - The canvas automatically scales itself to hold the number of loops being played.
 - The sound markers are assigned colors along the HSV spectrum to make the display a little more appealing for large numbers of tracks.
 - I deliberately chose two tracks that are the same length with an offset that produces a (very slow) meter and chord progression.
 - I used one of the [Teufelsberg impulse responses](http://www.balancemastering.com/blog/free-teufelsberg-nsa-listening-tower-impulse-responses-ir-irs-convolution/) from Balance Mastering, tweaked to double the length in Audacity via Paulstretch (2x, window of .001 sec).

See live demos [here]().

![Screenshot](dist/screenshot.png?raw=true)

Uses instrument samples from the [Sonatina Symphonic Orchestra](http://sso.mattiaswestlund.net/download.html). You can get more of them by downloading the ZIP from their site.

## Development

1. `npm install`
2. `npm run start`

This installs a live local server as well as a Babel compiler watcher. Changes in `src` are picked up automatically.

## Build and Deployment

To build the project, just invoke `npm run build`. Everything you need will be in the `dist` folder:

* `index.html` to host the application
* `musicforairport.js`, the compiled source code of the app.
* `musicforairports.min.js`, a minified version of the source code.
* `Samples` samples used to play the music and to generate the convolution reverb.

### Embedding

If you want to embed the player on an existing website, take a look at `index.html`. There are three key parts you need to take from there and add to your page:

* A `<canvas>` element with id `music-for-airports`.
* The whatwg-fetch polyfill and the Web Audio API shim libraries for cross-browser compatibility.
* The `musicforairports.js` or `musicforairports.min.js` script tag.

## License

ISC License

Original copyright (c) 2016, Tero Parviainen

This version copyright (c) 2018, Joe McMahon

Permission to use, copy, modify, and/or distribute this software for any purpose with or without fee is hereby granted, provided that the above copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
