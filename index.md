---
layout: default
splash:
  title: Cluster Garage
  quote: |
    Studios are passe for me. I'd rather play in a garage, in a truck, or a 
    rehearsal hall, a club, or a basement.
categories:
  columns: 3
  title: Come Play
  subtitle: Technology doesn't have to be boring
---

<div class="uk-section section-splash" data-uk-scrollspy="cls: uk-animation-slide-bottom-medium; repeat: true">
  <div class="uk-container splash-container">
    <img src="/assets/img/garage.jpg">
  </div>

  <div class="uk-container uk-container-xsmall">
    <blockquote cite="#">
    <p class="uk-margin-small-bottom">{{ page.splash.quote }}</p>
    <footer>Neil Young</footer>
    </blockquote>
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
