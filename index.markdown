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

    <div class="message-header">
        <p>{{ columna.title }} ({{ columna.date }})</p>
    </div>

    <div class="message-body">
        <div class="columns">
            <div class="column is-four-fifths">
                <p>{{ columna.title }} {{ columna.subtitle }}</p>
            </div>

    <div class="column">
        <button onClick="playMp3('https://archive.org/download/{{ columna.mp3 }}')" class="button is-danger has-left"> escuchar</button>
    </div>

    </div>

</div>
</article>

{% endfor %}

</div>
