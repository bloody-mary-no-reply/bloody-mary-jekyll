---
layout: home
---

<div class="container">

  {% include page-header.html title="Δημοσιεύσεις" %}

  <div class="article">
    <h2>Δημοσιεύσεις</h2>
    <h2><em>ΔΗΜΟΣΙΕΥΣΕΙΣ ΣΕ ΔΙΕΘΝΗ ΠΕΡΙΟΔΙΚΑ</em></h2>
      <table class="table table-striped">
        {% for pub in site.data.international_publications %}
          <tr>
            <td>
              {{ pub.authors }}. {{ pub.title }}. <i>{{ pub.magazine }}. {{ pub.year }} {% if pub.issue %}; {{pub.issue}} {% endif %} {% if pub.volume %}({{ pub.volume }}){% endif %}{% if pub.page_range %}: {{ pub.page_range }}{% endif %}</i>
            </td>
            <td>
              {% if pub.pfile_file_name %}
                <span class="label label-success">
                  <a href="{{ site.baseurl }}/assets/publications/{{ pub.pfile_file_name }}">Λήψη</a>
                </span>
              {% endif %}
            </td>
          </tr>
        {% endfor %}
      </table> 
    <br>
    <h2><em>ΔΗΜΟΣΙΕΥΣΕΙΣ ΣΕ ΕΛΛΗΝΙΚΑ ΠΕΡΙΟΔΙΚΑ</em></h2>
      <table class="table table-striped">
        {% for pub in site.data.greek_publications %}
          <tr>
            <td>
              {{ pub.authors }}. {{ pub.title }}. <i>{{ pub.magazine }}. {{ pub.year }} {% if pub.issue %}; {{pub.issue}} {% endif %} {% if pub.volume %}({{ pub.volume }}) {% endif %}{% if pub.page_range %}: {{ pub.page_range }}{% endif %}</i>
            </td>
            <td>
              {% if pub.pfile_file_name %}
                <span class="label label-success">
                  <a href="{{ site.baseurl }}/assets/publications/{{ pub.pfile_file_name }}">Λήψη</a>
                </span>
              {% endif %}
            </td>
          </tr>
        {% endfor %}
      </table>
    <br>
  </div>
</div>
