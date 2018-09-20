---
layout: default
splash:
  title: Cluster Garage
  subtitle: |
    Donec ut placerat purus, in gravida diam. Aliquam cursus metus urna, sit
    amet aliquet metus tristique vel. Curabitur ultricies laoreet turpis in
    imperdiet.
hero:
  title: ClusterGarage
  subtitle: Sed condimentum, nisi at efficitur dignissim
  search: false
section:
  title: In hac habitasse platea dictumst
  subtitle: |
    Suspendisse potenti. Integer nulla nibh, convallis vitae elit ac, tempor
    lobortis quam. Sed condimentum, nisi at efficitur dignissim, ex dui malesuada
    enim, ac convallis velit ex sed nunc. Aenean vitae tristique tellus. Proin at
    nibh suscipit, finibus lacus sed, pulvinar turpis. Phasellus viverra, libero
    sed ultricies varius, mauris nulla maximus nunc, id congue sapien erat sed
    nunc.
categories:
  columns: 2
  title: Products and Services
  subtitle: Morbi iaculis nunc eros, eget tempus mi tincidunt a.
---

{% if page.splash %}
<div class="uk-section section-splash" data-uk-scrollspy="cls: uk-animation-slide-bottom-medium; repeat: true">
  <div class="uk-container uk-container-small splash-container">
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

  <div class="uk-container uk-container-small">
		{% if page.splash.subtitle %}
		<p class="subtitle uk-text-lead uk-text-center">{{ page.splash.subtitle }}</p>
		{% endif %}
  </div>
</div>
{% endif %}

{% if page.section %}
<div class="uk-section uk-text-center">
	<div class="uk-container uk-container-small">
		{% if page.section.title %}
		<h2 class="uk-text-center heading-hero-2">{{ page.section.title }}</h2>
		{% endif %}
		{% if page.section.subtitle %}
    <p class="subtitle uk-text-lead uk-text-center">{{ page.section.subtitle | escape }}</p>
    {% endif %}
	</div>
</div>
{% endif %}

{% if page.categories.columns %}
    {% assign columns = page.categories.columns %}
{% else %}
    {% assign columns = 3 %}
{% endif %}

{% if page.categories %}
<div class="uk-section">
	<div class="uk-container">
    {% if page.categories.title %}
		<h2 class="uk-text-center heading-hero-2">{{ page.categories.title }}</h2>
		{% endif %}

		{% if page.categories.subtitle %}
    <p class="subtitle uk-text-lead uk-text-center">{{ page.categories.subtitle | escape }}</p>
    {% endif %}

		<div class="uk-child-width-1-{{ columns }}@m uk-grid-match uk-text-center uk-margin-medium-top" data-uk-grid>
		{% for item in site.data.navigation_home %}
			{% if item.title %}
			<div>
				<div class="uk-card uk-card-body uk-inline uk-border-rounded">
					<a class="uk-position-cover" href="{{ item.url | prepend:site.baseurl }}"></a>
					{% if item.icon %}
					<span data-uk-icon="icon: {{ item.icon }}; ratio: 2" class=""></span>
					{% endif %}
					<h3 class="uk-card-title uk-margin">{{ item.title }}</h3>
					{% if item.desc %}
					<p>{{ item.desc }}</p>
					{% endif %}
				</div>
      </div>
			{% endif %}
    {% endfor %}
    </div>
  </div>
</div>
{% endif %}
