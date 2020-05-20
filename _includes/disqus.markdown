{% if page.comments %}

Comments
---------------

{{ site.url }}{{ page.url | absolute_url }}

<div id="disqus_thread"></div>
<script>

var disqus_config = function () {
	this.page.url = '{{ site.url }}{{ page.url | absolute_url }}';
	{%- if page.disqus_id -%}
	this.page.identifier = '{{ page.disqus_id }}';
	{%- endif -%}
};
(function() { // DON'T EDIT BELOW THIS LINE
var d = document, s = d.createElement('script');
s.src = 'https://{{ site.disqus.shortname }}.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
               
			   
{% endif %}
