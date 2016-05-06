
# quaint-smartypants

Quotes, em/en dashes and ellipsis.

## Install

In your Quaint project directory, run the command:

    quaint --setup smartypants


## Sample configuration

```json
"smartypants": {
  "locale": "en"
}
```

## Features

Replace certain characters and sequences of characters by tidier
equivalents:

* `--` becomes the en dash character: –
* `---` becomes the em dash character: —
* `...` becomes the ellipsis character: …
* `***` becomes the asterism character: ⁂
* Single quotes `''` become curly quotes: `‘’`
* Specific to **en** locale:
  * `"..."` or `<<...>>` becomes curly quotes: `“...”`
* Specific to **fr** locale:
  * `"..."` or `<<...>>` becomes guillemets: `« ... »`
  * Insert non-breaking space before `!`, `?` and `:`.
  * `oe -> œ` and `Oe -> Œ`

In order to determine whether a quote is opening or closing,
quaint-smartypants checks whether it has a space before (in which case
it is an opening quote), or a space or punctuation after (in which
case it is a closing quote). Alternatively, can quote with angle
brackets like this: `<<...>>`, which will cause no ambiguities.


## Options

**locale**: either `en` (english, default) or `fr` (french), at least
for the moment. Locale changes quotation mark type and adds a few
language-specific rules. See the features section above.
