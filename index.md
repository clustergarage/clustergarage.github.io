---
layout: default
splash:
  title: Cluster Garage
  subtitle: Lorem ipsum dolor sit amet
hero:
  title: ClusterGarage
---

<div class="uk-section section-splash" data-uk-scrollspy="cls: uk-animation-slide-bottom-medium; repeat: true">
	<div class="uk-container uk-container-small">
		<h1 class="uk-heading-hero uk-text-center uk-margin-remove-top splash">
			{% for i in (0..40) %}
			<div class="text">
				<div class="text-inner1">
					<div class="text-inner2">{{ page.splash.title }}</div>
				</div>
			</div>
			{% endfor %}
		</h1>
	</div>

	{% if page.splash.subtitle %}
	<p class="subtitle uk-text-lead uk-text-center">{{ page.splash.subtitle }}</p>
	{% endif %}
</div>

