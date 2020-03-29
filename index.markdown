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

<article class="message">
    <a onClick="playMp3('https://archive.org/download/{{ columna.mp3 }}')">
    <div class="message-body">
    {% include play-circle.svg %} ({{ columna.date }}) {{ columna.title }} {{ columna.subtitle }} ({{ columna.min }}min)
    </div>
    </a>
</article>

{% endfor %}

</div>
