---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

<div class="container">
<div class="streaming">
    <audio id="audio" controls="controls">
        <source id="audioSource" src=""></source>
    </audio>
</div>
</div>

<div class="container">

{% for columna in site.data.columnas %}

<div class="box" onclick="playMp3('https://archive.org/download/{{ columna.mp3 }}')">
  <article class="media">
    <div class="media-left">
          {% include play-circle.svg %}
    </div>
    <div class="media-content">
      <div class="content">
        <p>
          <strong>{{ columna.title }}</strong>
          {{ columna.subtitle }}
          {{ columna.date }}
          ({{ columna.min }} min)
        </p>
      </div>
    </div>
  </article>
</div>

{% endfor %}

</div>
