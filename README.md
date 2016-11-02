# Exam: HTML & CSS

### Getting Started
 - Fork this repository under your own account
 - Commit your progress frequently and with descriptive commit messages
 - All your answers and solutions should go in this repository

### What can I use?
 - You can use any resource online, but **please work individually**
 - Instead of copy-pasting your answers and solutions, write them in your own words.


# Tasks

## 1. Build a design (~90 minutes) [10 points]
Build the following profile cards according to the design provided.   
Follow the design as closely as possible.   
Commit an HTML and a CSS file to this repository.
![design](exercise-1.png)

### Assets
John Duck | Jane Duck | Pencil icon
--------- | --------- | -----------
![duck](duck.jpg) | ![duck](duck2.jpg) | ![pencil-icon](edit-icon.png)   

### Other data
  - Name font size: 28 pixels
  - Text size: 14 pixels
  - Font family: Arial, sans-serif

### Acceptance criteria
The task is accepted if:
  - The result follows design [2p]
  - The code follows style guide [1p]
  - The CSS & HTML are valid [1p]
  - The HTML considers semantic responsibilities [2p]
  - The code avoids code duplication [2p]
  - The CSS has meaningful and short selectors [2p]

Extra points for if:
  - the result is centered on the page [2p]


## 2. Understand code (~15 minutes) [2 points]



Read the following code snippet:   
What is the distance between the top-left corner of the document body and the yellow box?   
Give a detailed explanation below!   
Add your answer to this readme file, commit your changes to this repository.

Answer:

The distance between the yellow box and the top-left corner of the body is from top: 40px, from left: 40px.

The yellow box is a child of the blue box. Both positions are absolute. The parent's absolute position resets the earlier positions. Therefore the yellow box positioned in the blue box (blue box top: 20px, left:20px). The blue box positioned in the body (body top: 20px left: 20px). The two boxes positions added and the result is: top: 40px left: 40px between the body top/left corner and the yellow box top-left corner.

A távolság a body jobb felső sarka és a yellow box között a body bal oldalától és a tetejétől 40-40px. A yellow box a blue box gyereke és mindkettő pozíciója absolute. Az absolute pozíció felülírja a korábbi pozíciót, így az azon belül lévő elemek a szülőhöz pozícionálnak. Jelen esetben a sárga szülője a kék, így az a kék jobb-felső sarkától 20-20px-re van. A kék viszont a body jobb-felső sarkától van 20-20px-re. A kettőt össze kell adni, így jön ki a 40-40px.

```HTML
<!DOCTYPE html>
<html>
  <head>
    <style>
      body {
        padding: 0px;
        margin: 0px;
      }
      .foo {
        top: 20px;
        left: 20px;
        width: 100px;
        height: 100px;
        position: absolute;
        background: blue;
      }
      .bar {
        top: 20px;
        left: 20px;
        width: 30px;
        height: 30px;
        position: absolute;
        background: yellow;
      }
    </style>
  </head>
  <body>
    <div class="foo">
      <div class="bar"></div>
    </div>
  </body>
</html>
```
#### Your answer: [2p]


## 3. Explain concepts (~15 minutes) [4 points]
Add your answer to this readme file, commit your changes to this repository.


### Explain the difference between `display: block` and `display: inline` in CSS! What is `display: inline-block`?
#### Your answer: [2p]

Answer:

display: block: It occupies the whole space of it's parent element. It starts in a new line and stretches out left and right as far as it can.

A block elem teljesen kitölti a szülő elem területét. Mindig új sorban kezdődik és a rendelkezésére álló terület határáig nyúlik.

display: inline: It can wrap some text inside the paragraph without disturbing the flow.

A bekezdés vagy szöveg eleme. Nem befolyásolja a dokumentum folyását, mivel nem foglalja el az egész teret, csak amennyi a saját kiterjedése. Nem kezdődik új sorban. Ilyen pl. az <a> elem.

display: inline-block: It generates a block inside the paragraph or text. The contant is flowed around it.

Hasonlóan működik, mint a block elem, csak a bekezdésen belül és nem foglalja el az egész sort, hanem, amennyi meg van adva számára.


### What is the difference between a `<section>` and an `<article>` element? Name one good example of using an `<article>`.
#### Your answer: [2p]

Answer:

section: It represents a generic section of a document. Mostly thematic grouping of the content.

Egy oldal, dokumentum főbb részeit tartalmazza. Főleg tematikusan összefüggő részeket tartalmaz.

article: It represents a self-contained part of the document. It can be a blog entry, forum post, magazine or newspaper article.

Egy önálló részét tartalmazza a dokumentumnak. Lehet egy cikk, blogbejegyzés, forum poszt stb.
