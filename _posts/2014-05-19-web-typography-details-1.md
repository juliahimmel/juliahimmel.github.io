---
layout: post
title: web typography details 1
---

It's easier than ever to get good typography on the web. The most visible manifestation of this is that we're no longer stuck with web-safe fonts. But really good typography is about the details. This is the first in a series of posts covering these details.

One simple thing that's adhered to in print design but often forgotten on the web is preventing line breaks in proper nouns, such as the names of corporations. For example, no word in Time Warner Inc. should not be allowed to wrap to the next line. You can achieve this like so:

HTML:

`<span class="nobreak">Time Warner Inc.</span>`

CSS:

`.nobreak { whitespace: nowrap; }`

Another relatively recent development is the ability to use finely controlled indents and hanging punctuation. The CSS `text-indent` property is part of CSS3. The most common indent in print is one em. This property can also be used to create the effect of hanging punctuation--that is, punctuation that hangs outside the margin of the text so that the letters are not knocked out of alignment. For example:

  <div class="quote">
    <h4 class="quote_body">&ldquo;After much pondering I think I understand a basic reason why a glass of something reviving is so welcome in the early evening. Partly, of course, it&rsquo;s just that, to revive, to relax; but it&rsquo;s also a convenient way of becoming a different person from your daytime self, less methodical, less calculating&#8212;however you put it, somebody different, and the prospect of that has helped to make the day tolerable.&rdquo;</h4>
  </div>

This can be achieved with a negative indent, in this case 0.3 em. You can also use JQuery to apply this dynamically.

