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

    <div class="message-body" onclick="playMp3('https://archive.org/download/{{ columna.mp3 }}')">
    {% include play-circle.svg %} ({{ columna.date }}) {{ columna.title }} {{ columna.subtitle }} ({{ columna.min }} min)
    </div>

</article>

{% endfor %}

</div>
