---
layout: page
title: Menu
permalink: /menu/
---

<!-- Deli classics -->
<div id="menu">

  <div class="pure-g">
  <div class="pure-u-1-3">
    <a href="/assets/img/deli-classic-6.jpg">
      <img style="border-radius: 10px;margin-bottom:10px" src="/assets/img/deli-classic-6.jpg" class="pure-img shrink-5-pct"/>
    </a>
    <center>
      <h2 class="menu-heading" style="font-size:24px">Wolf (1/4 lb)<br>$7.95</h2>
    </center>
  </div>

    <div class="pure-u-1-3">
      <a href="/assets/img/deli-classic-2.jpg">
        <img style="border-radius: 10px;margin-bottom:10px" src="/assets/img/deli-classic-2.jpg" class="pure-img shrink-5-pct"/>
      </a>
      <center>
        <h2 class="menu-heading" style="font-size:24px">Big Wolf (1/2 lb)<br>$11.95</h2>
      </center>
    </div>

    <div class="pure-u-1-3">
      <a href="/assets/img/deli-classic-7.jpg">
        <img style="border-radius: 10px;margin-bottom:10px" src="/assets/img/deli-classic-7.jpg" class="pure-img shrink-5-pct"/>
      </a>
      <center>
        <h2 class="menu-heading" style="font-size:24px">Big Bad Wolf (1 lb)<br>$20.95</h2>
      </center>
    </div>
  </div>

  <p>All of our sandwiches are served with a side of either coleslaw, or potato salad, and each of our sandwiches are served with a kosher pickle spear on the side.</p>

  <h2 class="menu-heading" style="font-size:32px">Deli classics</h2>

  <p>Each of our classic deli sandwiches are served on your choice of freshly baked rye, marble rye, or French bread, and your choice of mustard. At Big Wolf's, we have a wide variety of mustards including crowd favourites like dijon, jalapeño, and honey mustard!</p>

  <div class="pure-g">

    <!-- Meats -->
    <div class="pure-u-1-2">
      <h5 class="menu-heading" style="font-size:20px">Meats</h5>
      <ul style="list-style-type:none;margin:0px;padding:0px">
        {% for meat in site.data.menu.meats %}
          <li>{{ meat.name }}</li>
        {% endfor %}
      </ul>
    </div>

    <!-- Mustards -->
    <div class="pure-u-1-2">
      <h5 class="menu-heading" style="font-size:20px">Mustards</h5>
      <ul style="list-style-type:none;margin:0px;padding:0px">
        {% for mustard in site.data.menu.mustards %}
          <li>{{ mustard.name }}</li>
        {% endfor %}
      </ul>
    </div>
  </div>  

  <!-- 1x5 array of images showing the deli classics -->
  <div class="pure-g" style="margin-top:10px; margin-bottom:10px">
    <div class="pure-u-1-5"><a href="/assets/img/deli-classic-4.jpg"><img style="border-radius: 50%" src="/assets/img/deli-classic-4.jpg" class="pure-img shrink-5-pct"/></a></div>
    <div class="pure-u-1-5"><a href="/assets/img/deli-classic-1.jpg"><img style="border-radius: 50%" src="/assets/img/deli-classic-1.jpg" class="pure-img shrink-5-pct"/></a></div>
    <div class="pure-u-1-5"><a href="/assets/img/deli-classic-2.jpg"><img style="border-radius: 50%" src="/assets/img/deli-classic-2.jpg" class="pure-img shrink-5-pct"/></a></div>
    <div class="pure-u-1-5"><a href="/assets/img/deli-classic-3.jpg"><img style="border-radius: 50%" src="/assets/img/deli-classic-3.jpg" class="pure-img shrink-5 -pct"/></a></div>
    <div class="pure-u-1-5"><a href="/assets/img/deli-classic-5.jpg"><img style="border-radius: 50%" src="/assets/img/deli-classic-5.jpg" class="pure-img shrink-5-pct"/></a></div>
  </div>

  <!-- Chef inspired sandwiches -->
  <h2 class="menu-heading" style="font-size:32px">Chef inspired sandwiches</h2>
  <ul style="list-style-type:none;margin:0px;padding:0px">
    {% for e in site.data.menu.chef %}
      <li>
        <h5 class="menu-heading" style="font-size:20px;padding:0px;margin-top:5px;margin-bottom:5px">{{ e.name }}</h5>
        <p style="font-size:16px;padding:0px">{{ e.description }}</p>
      </li>
    {% endfor %}
  </ul>

  <!-- 1x5 array of images showing the chef inspired sandwiches -->
  <div class="pure-g" style="margin-top:10px; margin-bottom:10px">
    <div class="pure-u-1-5"><a href="/assets/img/chef-old-3.jpg"><img style="border-radius: 50%" src="/assets/img/chef-old-3.jpg" class="pure-img shrink-5-pct"/></a></div>
    <div class="pure-u-1-5"><a href="/assets/img/chef-old-2.jpg"><img style="border-radius: 50%" src="/assets/img/chef-old-2.jpg" class="pure-img shrink-5-pct"/></a></div>
    <div class="pure-u-1-5"><a href="/assets/img/chef-old-1.jpg"><img style="border-radius: 50%" src="/assets/img/chef-old-1.jpg" class="pure-img shrink-5-pct"/></a></div>
    <div class="pure-u-1-5"><a href="/assets/img/chef-old-4.jpg"><img style="border-radius: 50%" src="/assets/img/chef-old-4.jpg" class="pure-img shrink-5-pct"/></a></div>
    <div class="pure-u-1-5"><a href="/assets/img/chef-old-5.jpg"><img style="border-radius: 50%" src="/assets/img/chef-old-5.jpg" class="pure-img shrink-5-pct"/></a></div>
  </div>

  <!-- Create your own sandwiches -->
  <h2 class="menu-heading" style="font-size:32px">Create your own!</h2>

  <!-- First, count all of the items we have available -->
  {% capture number_of_breads %}{{ site.data.menu.breads | size }}{% endcapture %}
  {% capture number_of_proteins %}{{ site.data.menu.proteins | size }}{% endcapture %}
  {% capture number_of_toppings %}{{ site.data.menu.toppings | size }}{% endcapture %}
  {% capture number_of_sauces %}{{ site.data.menu.sauces | size }}{% endcapture %}
  {% capture number_of_cheeses %}{{ site.data.menu.cheese | size }}{% endcapture %}
  {% capture number_of_extras %}{{ site.data.menu.extras | size }}{% endcapture %}

  <!-- A friendly blurb that talks about how many different options guests have -->
  At Big Wolf's, we love to see you get creative! With {{ number_of_breads }} different types of bread delivered fresh every morning, {{ number_of_proteins }} different protein options, {{ number_of_toppings }} toppings, {{ number_of_sauces }} sauces, {{ number_of_cheeses }} cheeses, and little extras like {{ site.data.menu.extras[1].name | downcase }} or {{ site.data.menu.extras[2].name | downcase }}, the sky is the limit!

  <!-- Guests can chose from a smörgåsbord of meats, breads, toppings, and sauces -->
  <div class="pure-g">

    <!-- Left column -->
    <div class="pure-u-1-2">

      <!-- Breads -->
      <h5 class="menu-heading" style="font-size:20px">Breads</h5>
      <ul style="list-style-type:none;margin:0px;padding:0px">
        {% for e in site.data.menu.breads %}
          <li><p style="font-size:16px;padding:0px;margin:0px">{{ e.name }}</p></li>
        {% endfor %}
      </ul>

      <!-- Toppings -->
      <h5 class="menu-heading" style="font-size:20px">Toppings</h5>
      <ul style="list-style-type:none;margin:0px;padding:0px">
        {% for e in site.data.menu.toppings %}
          <li><p style="font-size:16px;padding:0px;margin:0px">{{ e.name }}</p></li>
        {% endfor %}
      </ul>

      <!-- Cheese -->
      <h5 class="menu-heading" style="font-size:20px">Cheese</h5>
      <ul style="list-style-type:none;margin:0px;padding:0px">
        {% for e in site.data.menu.cheese %}
          <li><p style="font-size:16px;padding:0px;margin:0px">{{ e.name }}</p></li>
        {% endfor %}
      </ul>

      <!-- Extra items -->
      <table style="width:100%">
        <tr>
          <td><h5 class="menu-heading" style="font-size:20px">Extras</h5></td>
          <td></td>
          <td><h5 class="menu-heading" style="font-size:16px;padding:0px;margin:0px;">Each</h5></td>
        </tr>
        {% for e in site.data.menu.extras %}
          {% if e.price %}
            <tr>
              <td><p style="font-size:16px;padding:0px;margin:0px">{{ e.name }}</p></td>
              <td></td>
              <td>{{ e.price }}</td>
            </tr>
          {% endif %}
        {% endfor %}
      </table>
    </div>

    <!-- Right column -->
    <div class="pure-u-1-2">
      <!-- Protein -->
      <h5 class="menu-heading" style="font-size:20px">Protein</h5>
      <ul style="list-style-type:none;margin:0px;padding:0px">
        {% for e in site.data.menu.proteins %}
          <li><p style="font-size:16px;padding:0px;margin:0px">{{ e.name }}</p></li>
        {% endfor %}
      </ul>

      <!-- Sauces -->
      <h5 class="menu-heading" style="font-size:20px">Sauces</h5>
      <ul style="list-style-type:none;margin:0px;padding:0px">
        {% for e in site.data.menu.sauces %}
          <li><p style="font-size:16px;padding:0px;margin:0px">{{ e.name }}</p></li>
        {% endfor %}
      </ul>
    </div>
  </div>

  <!-- 1x5 array of images showing the meats, toppings, etc. available -->
  <div class="pure-g" style="margin-top:10px; margin-bottom:10px">
    <div class="pure-u-1-5"><a href="/assets/img/create-1.jpg"><img style="border-radius: 50%" src="/assets/img/create-1.jpg" class="pure-img shrink-5-pct"/></a></div>
    <div class="pure-u-1-5"><a href="/assets/img/create-2.jpg"><img style="border-radius: 50%" src="/assets/img/create-2.jpg" class="pure-img shrink-5-pct"/></a></div>
    <div class="pure-u-1-5"><a href="/assets/img/create-3.jpg"><img style="border-radius: 50%" src="/assets/img/create-3.jpg" class="pure-img shrink-5-pct"/></a></div>
    <div class="pure-u-1-5"><a href="/assets/img/create-4.jpg"><img style="border-radius: 50%" src="/assets/img/create-4.jpg" class="pure-img shrink-5-pct"/></a></div>
    <div class="pure-u-1-5"><a href="/assets/img/create-5.jpg"><img style="border-radius: 50%" src="/assets/img/create-5.jpg" class="pure-img shrink-5-pct"/></a></div>
  </div>

  <!-- Sides -->
  <table style="width:100%">
    <tr>
      <td><h2 class="menu-heading" style="; font-size:32px">Sides</h2></td>
      <td><h5 class="menu-heading" style="font-size:16px;padding:0px;margin:0px;">8 oz.</h5></td>
      <td><h5 class="menu-heading" style="font-size:16px;padding:0px;margin:0px;">16 oz.</h5></td>
    </tr>
    {% for e in site.data.menu.sides %}
      {% if e.small or e.large %}
        <tr>
          <td><p style="font-size:16px;padding:0px;margin:0px">{{ e.name }}</p></td>
          <td>{{ e.small }}</td>
          <td>{{ e.large }}</td>
        </tr>
      {% endif %}
    {% endfor %}

    <!-- A la carte items -->
    <tr>
      <td></td>
      <td><h5 class="menu-heading" style="font-size:16px;padding:0px;margin:0px">Each</h5></td>
      <td></td>
    </tr>

    {% for e in site.data.menu.sides %}
      {% if e.price %}
        <tr>
          <td><p style="font-size:16px;padding:0px;margin:0px">{{ e.name }}</p></td>
          <td>{{ e.price }}</td>
          <td></td>
        </tr>
      {% endif %}
    {% endfor %}
  </table>

  <!-- Kids menu -->
  <h2 class="menu-heading" style="; font-size:32px">Kids menu</h2>

  <div class="pure-g" style="margin-top:10px; margin-bottom:10px">
    <div class="pure-u-4-5">

      <ul style="list-style-type:none;margin:0px;padding:0px">
        {% for e in site.data.menu.kids %}
          <li>
            <h5 class="menu-heading" style="font-size:20px;padding:0px;margin:0px;">{{ e.name }}</h5>
            <p style="font-size:16px;padding:0px">{{ e.description }}</p>
          </li>
        {% endfor %}
      </ul>
    </div>
    <div class="pure-u-1-5">
      <a href="/assets/img/little-wolf.jpg"><img style="border-radius: 50%" src="/assets/img/little-wolf.jpg" class="pure-img shrink-5-pct"/></a>
    </div>
  </div>
</div>
