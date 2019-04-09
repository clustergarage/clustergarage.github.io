---
layout: default
splash:
  title: Cluster Garage
  subtitle: |
    Donec ut placerat purus, in gravida diam. Aliquam cursus metus urna, sit
    amet aliquet metus tristique vel. Curabitur ultricies laoreet turpis in
    imperdiet.
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
  columns: 3
  title: Products and Services
  subtitle: Morbi iaculis nunc eros, eget tempus mi tincidunt a.
---

<div class="uk-section section-splash" data-uk-scrollspy="cls: uk-animation-slide-bottom-medium; repeat: true">
  <div class="uk-container splash-container">
    <img src="/assets/img/garage.jpg">
  </div>

  <div class="uk-container uk-container-small">
    <p class="subtitle uk-text-lead uk-text-center">{{ page.splash.subtitle }}</p>
  </div>
</div>

<div class="uk-section uk-text-center">
  <div class="uk-container uk-container-small">
    <h2 class="uk-text-center heading-hero-2">{{ page.section.title }}</h2>
    <p class="subtitle uk-text-lead uk-text-center">{{ page.section.subtitle | escape }}</p>
  </div>
</div>

{% assign columns = page.categories.columns %}

<div class="uk-section">
  <div class="uk-container">
    <h2 class="uk-text-center heading-hero-2">{{ page.categories.title }}</h2>

    <p class="subtitle uk-text-lead uk-text-center">{{ page.categories.subtitle | escape }}</p>

    <div class="uk-child-width-1-{{ columns }}@m uk-grid-match uk-text-center uk-margin-medium-top" data-uk-grid>
    {% for item in site.data.navigation_home %}
      <div>
        <div class="uk-card uk-card-body uk-inline uk-border-rounded">
          <a class="uk-position-cover" href="{{ item.url | prepend:site.baseurl }}"></a>
          <span data-uk-icon="icon: {{ item.icon }}; ratio: 2"></span>
          <h3 class="uk-card-title uk-margin">{{ item.title }}</h3>
          <p>{{ item.desc }}</p>
        </div>
      </div>
    {% endfor %}
    </div>
  </div>
</div>
