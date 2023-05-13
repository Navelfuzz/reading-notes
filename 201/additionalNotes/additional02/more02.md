# Basics of HTML, CSS & JS

## Advanced HTML Text Formatting

Headings are simply just pre-formatted section splitters. The number `h1` through `h6`.
`h1` is the main heading, `h2` is subheadings, `h3` are sub-headings.

***Structural Hierarchy Example***

    <h1>The Crushing Bore</h1>
        <p>By Chris Mills</p>
    <h2>Chapter 1: The dark night</h2>
      <p>
        It was a dark night. Somewhere, an owl hooted. The rain lashed down on the…
      </p>
    <h2>Chapter 2: The eternal silence</h2>
      <p>Our protagonist could not so much as a whisper out of the shadowy figure…</p>
    <h3>The specter speaks</h3>
      <p>
        Several more hours had passed, when all of a sudden the specter sat bolt
        upright and exclaimed, "Please have mercy on my soul!"
      </p>

### Why use Span?

    <span style="font-size: 32px; margin: 21px 0; display: block;">
      Is this a top level heading?
    </span>

This is a `<span>` element. It has no semantics. You use it to wrap content when you want to
apply CSS to it (or do something to it with JavaScript) without giving it any extra meaning.
(You'll find out more about these later on in the course.) We've applied some CSS to it
to make it look like a top level heading, but since it has no semantic value, it will
not get any of the extra benefits described above. It is a good idea to use the relevant
HTML element for the job.

## *Lists*

### Unordered

Unordered lists use the `<ul>` element wrapped around all entirety of the list. `<li>` is
wrapped around each individual item:

    <ul>
      <li>milk</li>
      <li>eggs</li>
      <li>bread</li>
      <li>hummus</li>
    </ul>

### Ordered

    <ol>
      <li>Drive to the end of the road</li>
      <li>Turn right</li>
      <li>Go straight across the first two roundabouts</li>
      <li>Turn left at the third roundabout</li>
      <li>The school is on your right, 300 meters up the road</li>
    </ol>

***Nested Lists***

    <ol>
      <li>Remove the skin from the garlic, and chop coarsely.</li>
      <li>Remove all the seeds and stalk from the pepper, and chop coarsely.</li>
      <li>Add all the ingredients into a food processor.</li>
      <li>
        Process all the ingredients into a paste.
        <ul>
          <li>
            If you want a coarse "chunky" hummus, process it for a short time.
          </li>
          <li>If you want a smooth hummus, process it for a longer time.</li>
        </ul>
      </li>
    </ol>

## Emphasis and Importance

***Emphasis*** the `<em>` tag: works with accessibility features (voice readers). This
displays the text as italic, however, don't use it purely for that. Perhaps use `<span>` or
`<i>` for that. `<em>` can be used to accomplish more.

***Strong*** the `<strong>` tag: similar to `<em>` it changes the on screen text (to bold)
but has other implications in terms of accessibility. To purely use bold styling use
`<span>` or `<b>`.

### Italic, bold, underline…

The elements we've discussed so far have clearcut associated semantics. The situation
with `<b>`, `<i>`, and `<u>` is somewhat more complicated. They came about so people could
write bold, italics, or underlined text in an era when CSS was still supported poorly
or not at all. Elements like this, which only affect presentation and not semantics, are
known as presentational elements and should no longer be used because, as we've
seen before, semantics is so important to accessibility, SEO, etc.

HTML5 redefined `<b>`, `<i>`, and `<u>` with new, somewhat confusing, semantic roles.

Here's the best rule you can remember: It's only appropriate to use `<b>`, `<i>`, or `<u>` to
convey a meaning traditionally conveyed with bold, italics, or underline when there isn't
a more suitable element; and there usually is. Consider whether `<strong>`, `<em>`, `<mark>`,
 or `<span>` might be more appropriate.

Always keep an accessibility mindset. The concept of italics isn't very helpful to people using screen readers, or to people using a writing system other than the Latin alphabet.

`<i>` is used to convey a meaning traditionally conveyed by italic: foreign words,
taxonomic designation, technical terms, a thought…
`<b>` is used to convey a meaning traditionally conveyed by bold: keywords, product
 names, lead sentence…
`<u>` is used to convey a meaning traditionally conveyed by underline: proper name,
 misspelling…

## Other Examples Scientifit, Foreign Language, Misspelling, Definitions

    <!-- scientific names -->
    <p>
      The Ruby-throated Hummingbird (<i>Archilochus colubris</i>) is the most common
      hummingbird in Eastern North America.
    </p>

    <!-- foreign words -->
    <p>
      The menu was a sea of exotic words like <i lang="uk-latn">vatrushka</i>,
      <i lang="id">nasi goreng</i> and <i lang="fr">soupe à l'oignon</i>.
    </p>

    <!-- a known misspelling -->
    <p>Someday I'll learn how to <u class="spelling-error">spel</u> better.</p>

    <!-- term being defined when used in a definition -->
    <dl>
      <dt>Semantic HTML</dt>
      <dd>
        Use the elements based on their <b>semantic</b> meaning, not their
        appearance.
      </dd>
    </dl>

___

## Description Lists

Description lists use a different wrapper than the other list types -- `<dl>`; in addition
each term is wrapped in a `<dt>` (description term) element, and each description is
wrapped in a `<dd>`.

*Example*: Note that the finale `<dt>` has multiple descriptions.

    <dl>
      <dt>soliloquy</dt>
      <dd>
        In drama, where a character speaks to themselves, representing their inner
        thoughts or feelings and in the process relaying them to the audience (but
        not to other characters.)
      </dd>
      <dt>monologue</dt>
      <dd>
        In drama, where a character speaks their thoughts out loud to share them
        with the audience and any other characters present.
      </dd>
      <dt>aside</dt>
      <dd>
        In drama, where a character shares a comment only with the audience for
        humorous or dramatic effect. This is usually a feeling, thought, or piece of
        additional background information.
      </dd>
      <dd>
        In writing, a section of content that is related to the current topic, but
        doesn't fit directly into the main flow of content so is presented nearby
        (often in a box off to the side.)
      </dd>
    </dl>

## Quotations

### Blockquotes

If a section of ablock level content (paragraph, or multiple paragraphs, a list, etc...) is
quoted from somewhere else, you should wrap it inside a `<blockquote>` element to
signify this, and include a URL pointing to the source of the quote inside a `cite`
attribute. The following markup is taken from the MDN `<blockquote>` element page.

    <p>
      The <strong>HTML <code>&lt;blockquote&gt;</code> Element</strong> (or
      <em>HTML Block Quotation Element</em>) indicates that the enclosed text is an
      extended quotation.
    </p>

To turn this into a block quote:

    <p>Here is a blockquote:</p>
    <blockquote
      cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote">
      <p>
        The <strong>HTML <code>&lt;blockquote&gt;</code> Element</strong> (or
        <em>HTML Block Quotation Element</em>) indicates that the enclosed text is
        an extended quotation.
      </p>
    </blockquote>

![Blockquote Example](blockquote.png)

### Inline Quotations

Inline quotations work exactly the same with the `<q>` element.

    <p>
      The quote element — <code>&lt;q&gt;</code> — is
      <q cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q">
        intended for short quotations that don't require paragraph breaks.
      </q>
    </p>

![Inline Quotation](inlineQuote.png)

### Citations

The content of the `cite` attribute cannot be linked (downside):

    <p>
      According to the
      <a href="/en-US/docs/Web/HTML/Element/blockquote">
        <cite>MDN blockquote page</cite></a>:
    </p>

    <blockquote
      cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote">
      <p>
        The <strong>HTML <code>&lt;blockquote&gt;</code> Element</strong> (or
        <em>HTML Block Quotation Element</em>) indicates that the enclosed text is
        an extended quotation.
      </p>
    </blockquote>

    <p>
      The quote element — <code>&lt;q&gt;</code> — is
      <q cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q">
        intended for short quotations that don't require paragraph breaks.
      </q>
      — <a href="/en-US/docs/Web/HTML/Element/q"><cite>MDN q page</cite></a>.
    </p>

Citations are italic by default.

![Citation](citation.png)

## Abbreviations

`<abbr>` is the abbreviation element. Used to wrap abbreviations or acronyms. Then provide
full expansion of the term in plain text on the first use.

*Example*

    <p>
      We use <abbr>HTML</abbr>, Hypertext Markup Language, to structure our web
      documents.
    </p>

    <p>
      I think <abbr title="Reverend">Rev.</abbr> Green did it in the kitchen with
      the chainsaw.
    </p>

Looks like:

![Abbreviation Example](abbreviation.png)

## Contact Details

    <address>
      <p>
        Chris Mills<br />
        Manchester<br />
        The Grim North<br />
        UK
      </p>

      <ul>
        <li>Tel: 01234 567 890</li>
        <li>Email: me@grim-north.co.uk</li>
      </ul>
    </address>

*Also this works:*

    <address>
      Page written by <a href="../authors/chris-mills/">Chris Mills</a>.
    </address>

**Note:** *The* `<address>` *element should only be used to provide contact information
for the document contained with the nearest* `<article>` *or* `<body>` *element. It would be
correct to use it in the footer of a site to include the contact information of the entire
site, or inside an article for the contact details of the author, but not to mark up a list
of addresses unrelated to the content of that page.*

## Superscript and Subscript

`<sup>` : superscripts; `<sub>` : subscripts

    <p>My birthday is on the 25<sup>th</sup> of May 2001.</p>
    <p>
      Caffeine's chemical formula is
      C<sub>8</sub>H<sub>10</sub>N<sub>4</sub>O<sub>2</sub>.
    </p>
    <p>If x<sup>2</sup> is 9, x must equal 3 or -3.</p>

The output of this code looks like so:

![Super and Sub scripts](supSub.png)

## Representing Computer Code

`<code>`: For marking up generic pieces of computer code.
`<pre>`: For retaining whitespace (generally code blocks) — if you use indentation or excess
whitespace inside your text, browsers will ignore it and you will not see it on your
rendered page. If you wrap the text in `<pre>``</pre>` tags however, your whitespace will
be rendered identically to how you see it in your text editor.
`<var>`: For specifically marking up variable names.
`<kbd>`: For marking up keyboard (and other types of) input entered into the computer.
`<samp>`: For marking up the output of a computer program.

    <pre><code>const para = document.querySelector('p');
    
    para.onclick = function() {
      alert('Owww, stop poking me!');
    }</code></pre>
    
    <p>
      You shouldn't use presentational elements like <code>&lt;font&gt;</code> and
      <code>&lt;center&gt;</code>.
    </p>
    
    <p>
      In the above JavaScript example, <var>para</var> represents a paragraph
      element.
    </p>
    
    <p>Select all the text with <kbd>Ctrl</kbd>/<kbd>Cmd</kbd> + <kbd>A</kbd>.</p>
    
    <pre>$ <kbd>ping mozilla.org</kbd>
    <samp>PING mozilla.org (63.245.215.20): 56 data bytes
    64 bytes from 63.245.215.20: icmp_seq=0 ttl=40 time=158.233 ms</samp></pre>









