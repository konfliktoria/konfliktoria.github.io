---
layout: post
title: Bildergalerie
subtitle: Test
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
author: Viki
---

Hier steht ein bisschen Text und dann schauen wir mal, ob das hier funktioniert.

{% assign image_list = "Mongolei.jpeg,path.jpg,crepe.jpg" | split: "," %}
<div class="swiper">
  <div class="swiper-wrapper">
    {% for img in image_list %}
      <div class="swiper-slide">
        <img src="{{ '/assets/img/' | append: img | relative_url }}" alt="{{ img }}">
      </div>
    {% endfor %}
  </div>
  <div class="swiper-button-next"></div>
  <div class="swiper-button-prev"></div>
  <div class="swiper-pagination"></div>
</div>


