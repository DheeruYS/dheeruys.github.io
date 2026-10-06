<h2 id="photography" style="margin: 2px 0px 10px;">Photography</h2>

<div class="photo-grid">
{% for p in site.data.photos.main %}
<figure>
  <a href="{{ p.file }}" target="_blank"><img src="{{ p.file }}" alt="{{ p.caption }}" loading="lazy"></a>
  {% if p.caption %}<figcaption>{{ p.caption }}</figcaption>{% endif %}
</figure>
{% endfor %}
</div>

<style>
.photo-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(160px, 1fr)); gap: 12px; }
.photo-grid figure { margin: 0; }
.photo-grid img { width: 100%; aspect-ratio: 1; object-fit: cover; border-radius: 6px; display: block; }
.photo-grid figcaption { font-size: 13px; text-align: center; margin-top: 4px; opacity: 0.7; }
</style>
