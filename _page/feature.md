---
layout: default
---
# Site Feature

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](/page/another-page).

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

<style>
/* === WRAPPER OTOMATIS === */
.pre-wrapper {
  display: grid;
  grid-template-columns: auto 1fr;
  background: #1e1e1e;
  border: 1px solid #444;
  border-radius: 8px;
  overflow: auto;
  font-size: 14px;
  line-height: 1.5;
  margin: 20px 0;
}

/* === LINE NUMBERS === */
.pre-wrapper .line-numbers {
  background: #252526;
  color: #858585;
  text-align: right;
  padding: 12px 10px 12px 12px;
  user-select: none;
  border-right: 1px solid #444;
  position: sticky;
  left: 0;
  z-index: 10;
}

.pre-wrapper .line-numbers span {
  display: block;
  line-height: 1.5;
  font-family: Consolas, monospace;
}

/* === KODE === */
.pre-wrapper pre {
  margin: 0;
  padding: 12px;
  overflow: visible;
}

.pre-wrapper pre code span {
  display: block;
  white-space: pre;
  line-height: 1.5;
}

/* highlight baris saat hover */
.pre-wrapper pre code span:hover {
  background: #2a2a2a;
}
</style>

<script>
document.addEventListener("DOMContentLoaded", () => {
  document.querySelectorAll("pre > code").forEach(code => {
    const pre = code.parentElement;
    const lines = code.textContent.replace(/\n$/, "").split("\n");

    // Bungkus PRE dalam .pre-wrapper
    const wrapper = document.createElement("div");
    wrapper.className = "pre-wrapper";

    // Buat kolom kiri (nomor baris)
    const nums = document.createElement("div");
    nums.className = "line-numbers";

    nums.innerHTML = lines.map((_, i) => `<span>${i + 1}</span>`).join("");

    // Ganti setiap baris kode menjadi span
    code.innerHTML = lines.map(line => `<span>${line || " "}</span>`).join("\n");

    // Masukkan DOM baru
    pre.replaceWith(wrapper);
    wrapper.appendChild(nums);
    wrapper.appendChild(pre);
  });
});
</script>

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three | head1        | head two          | three |
|:-------------|:------------------|:------|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  | ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  | out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   | ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  | ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### A button

<button id="btn">Klik saya</button>

<script>
document.getElementById("btn").addEventListener("click", () => {
  alert("Halo dari JS!");
});
</script>

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://i.postimg.cc/VvnwvXZ9/premium-photo-1700752853984-d3d1574aabd2.jpg)

### Definition lists can be used with HTML syntax.

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
