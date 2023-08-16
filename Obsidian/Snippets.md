---
source: https://obsidian-snippets.pages.dev/snippets/pdf-export-tweaks/
---

CSS-Bausteine können in `[vault]/.obsidian/snippets/[name].css` hinterlegt werden

## Page Break on `---`

```css
@media print {
  hr {
	  break-after:page;
	  visibility: hidden;
  }
}
```


## Prevent Headings from being on bottom of Page


```css
@media print {
  h1:after, h3:after, h2:after, h4:after, h5:after, h6:after{
     content: "";
    display: block;
    height: 100px;
    margin-bottom: -100px;
	}	
}
```

