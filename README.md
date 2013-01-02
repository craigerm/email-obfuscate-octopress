# Introduction

This is plugin for Octopress that will obfuscate an email address by adding
an email tag to markdown.

## Usage

```
{% email test@example.com %}
```

## Installation

Copy 'email.rb' to your 'plugins directory'

## How it Works

The plugin will render a small javascript block that performs an inline document.write. 
It renders an email address with some characters encoded and in reverse order. It then
uses CSS to re-reverse the email to display to the user.

For example this markdown:

```
Please email me at: {% email test@example.com %}
```

will render this html:

```html
Please email me at: 
<script type="text/javascript"> document.write('<a style="unicode-bidi:
bidi-override; direction: rtl;"
href="&#109;&#97;&#105;&#108;&#116;&#111;&#58;test&#64;example&#46;com">moc&#46;elpmaxe&#64;tset</a>');
</script> 
```

## License

Copyright (c) 2013 Craig MacGregor

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
of the Software, and to permit persons to whom the Software is furnished to do
so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
