---
{"dg-publish":true,"permalink":"/words/advanced-slides/","dgPassFrontmatter":true}
---


## 主要功能

-   Live Preview while editing your slides markdown
-   Theme support for your slides
-   Embed Support - include other Markdown documents in slides - 
- `![[Note.md#FirstChapter]]`
-   Image Support
    -   include images through Obsidian Synthax - `![[picture.jpg]]`
    -   pipe image properties - - `![[image.png|100x100]]`
-   Block Support - `::: block`
-   Footnote Support - `Here's a footnote[^1]`
-   Define stylesheets inside Markdown - `<style>....</style>`
-   Pass options To Slide Compiler through frontmatter
-   Annotate elements `<!-- element class="red" -->`
-   Support for internal links
    -   `[[Note]]` will be rendered as normal text in Presentation
    -   with aliases `[[Note|My Note]]`
-   Excalidraw Support
-   Mermaid Support

---
title: "ML Ops"
center: true
theme: black
---
### 我的Notion共享
<grid drop="0 8" drag="100 92">

<iframe id="mlops" width="100%" height="100%" data-src="https://marbled-popcorn-fba.notion.site/bb0bfe74365646399030ca4891ff3114" data-preload data-background-interactive></iframe>

</grid>
---
使用代码
```
<grid drop="0 8" drag="100 92">

<iframe id="mlops" width="100%" height="100%" data-src="https://marbled-popcorn-fba.notion.site/bb0bfe74365646399030ca4891ff3114" data-preload data-background-interactive></iframe>

</grid>
```

---
>[!note]- 向下翻页（减号多少）
>```
># Slide 1
>---
># Slide 2.1
>--
># Slide 2.2
>---
>


示例
# Slide 1
---
# Slide 2.1
--
# Slide 2.2

---
<!-- .slide: style="background-color: coral;" -->

## Header with coral background color

Paragraph has coral background color, too!

---

<!-- .slide: style="background-color: green;" -->

- All Bullet points
- have green
- background color

---
### 渐入渐出
```
渐入 <!-- element class="fragment" -->

渐出 <!-- element class="fragment fade-out" -->

红色高亮 <!-- element class="fragment highlight-red" -->

渐入，然后出 <!-- element class="fragment fade-in-then-out" -->

飞入 <!-- element class="fragment fade-up" -->
```
---

### 先后展示
```
- Permanent item
- Appear Fourth <!-- element class="fragment" data-fragment-index="4" -->
- Appear Third <!-- element class="fragment" data-fragment-index="3" -->
- Appear Second <!-- element class="fragment" data-fragment-index="2" -->
- Appear First <!-- element class="fragment" data-fragment-index="1" -->
```
---
> [!note]-  列表动画

### 展开
```
# Unordered list

- First
- Second
- Third

---

# Fragmented unordered list

- Permanent
+ First
+ Second
+ Third

---

# Ordered list

1. First
2. Second
3. Third

---

# Fragmented ordered list

1. Permanent
2) Second
3) Third
4) Fourth

```


### excalidraw支持
```
![[Sample.excalidraw\|100]]

![[Sample.excalidraw\|Sample.excalidraw]] <!-- element style="width:300px; height:400px" -->

```
