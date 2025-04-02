---
layout: post
title:  "CSS Tutorial"
date:   2025-03-14 12:57:11 +0100
categories: jekyll update
---
## Animacion con CSS

```bash
#myDIV {

  border: 1px solid red;;
  animation: mymove 2s infinite;

}

@keyframes mymove {
  50% {border: 20px solid lightblue;}
    75% {border-color: blue;}
    25% {border-color: black;}
  50% {box-shadow: 10px 20px 30px blue;}
  50% {color: blue;}
}

```

<style>
#myDIV {

  border: 1px solid red;;
  animation: mymove 2s infinite;

}

@keyframes mymove {
  50% {border: 20px solid lightblue;}
    75% {border-color: blue;}
    25% {border-color: black;}
  50% {box-shadow: 10px 20px 30px blue;}
  50% {color: blue;}
}
</style>

<p id ="myDIV">Esto es un ejemplo de CSS </p>