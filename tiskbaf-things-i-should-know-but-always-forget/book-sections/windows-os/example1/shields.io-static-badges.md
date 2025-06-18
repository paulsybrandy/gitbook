# shields.io - static badges

The static badge accepts a single required path parameter which encodes either:

* Label, message and color separated by a dash `-`. For example:\
  ![any text: you like](https://img.shields.io/badge/any\_text-you\_like-blue) - [https://img.shields.io/badge/any\_text-you\_like-blue](https://img.shields.io/badge/any\_text-you\_like-blue)
* Message and color only, separated by a dash `-`. For example:\
  ![just the message](https://img.shields.io/badge/just%20the%20message-8A2BE2) - [https://img.shields.io/badge/just%20the%20message-8A2BE2](https://img.shields.io/badge/just%20the%20message-8A2BE2)

| URL input               | Badge output   |
| ----------------------- | -------------- |
| Underscore `_` or `%20` | Space          |
| Double underscore `__`  | Underscore `_` |
| Double dash `--`        | Dash `-`       |

Hex, rgb, rgba, hsl, hsla and css named colors may be used.

| Path Parameters                                                                                                                                                                           |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><code>badgeContent</code> string — <strong>REQUIRED</strong></p><p>Label, (optional) message, and color. Separated by dashes</p><p>Example: <code>build-passing-brightgreen</code></p> |

| Query Parameters                                                                                                                                                                                                                                                                                                                                                                                                                 |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><code>style</code> string</p><p><strong>Possible values:</strong> [<code>flat</code>, <code>flat-square</code>, <code>plastic</code>, <code>for-the-badge</code>, <code>social</code>]</p><p>If not specified, the default style for this badge is "flat".</p><p>Example: <code>flat</code></p>                                                                                                                               |
| <p><code>logo</code> string</p><p>Icon slug from simple-icons. You can click the icon title on <a href="https://simpleicons.org/">simple-icons</a> to copy the slug or they can be found in the <a href="https://github.com/simple-icons/simple-icons/blob/master/slugs.md">slugs.md file</a> in the simple-icons repository. <a href="https://shields.io/docs/logos">Further info</a>.</p><p>Example: <code>appveyor</code></p> |
| <p><code>logoColor</code> string</p><p>The color of the logo (hex, rgb, rgba, hsl, hsla and css named colors supported). Supported for simple-icons logos but not for custom logos.</p><p>Example: <code>violet</code></p>                                                                                                                                                                                                       |
| <p><code>logoSize</code> string</p><p>Make icons adaptively resize by setting <code>auto</code>. Useful for some wider logos like <code>amd</code> and <code>amg</code>. Supported for simple-icons logos but not for custom logos.</p><p>Example: <code>auto</code></p>                                                                                                                                                         |
| <p><code>label</code> string</p><p>Override the default left-hand-side text (<a href="https://developer.mozilla.org/en-US/docs/Glossary/percent-encoding">URL-Encoding</a> needed for spaces or special characters!)</p><p>Example: <code>healthiness</code></p>                                                                                                                                                                 |
| <p><code>labelColor</code> string</p><p>Background color of the left part (hex, rgb, rgba, hsl, hsla and css named colors supported).</p><p>Example: <code>abcdef</code></p>                                                                                                                                                                                                                                                     |
| <p><code>color</code> string</p><p>Background color of the right part (hex, rgb, rgba, hsl, hsla and css named colors supported).</p><p>Example: <code>fedcba</code></p>                                                                                                                                                                                                                                                         |
| <p><code>cacheSeconds</code> string</p><p>HTTP cache lifetime (rules are applied to infer a default value on a per-badge basis, any values specified below the default will be ignored).</p><p>Example: <code>3600</code></p>                                                                                                                                                                                                    |
| <p><code>link</code> string[]</p><p>Specify what clicking on the left/right of a badge should do. Note that this only works when integrating your badge in an <code>&#x3C;object></code> HTML tag, but not an <code>&#x3C;img></code> tag or a markup language.</p>                                                                                                                                                              |
