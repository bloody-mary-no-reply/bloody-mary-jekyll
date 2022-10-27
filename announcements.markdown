---
layout: home
---

<div class="container">

  {% include page-header.html title="Ανακοινώσεις - Περιλήψεις" %}

  <div class="article">
    <h2>Ανακοινώσεις - Περιλήψεις</h2>
    <h2><em>ΔΙΕΘΝΗ ΣΥΝΕΔΡΙΑ</em></h2>
      <table class="table table-striped">
        {% for ann in site.data.international_announcements %}
          <tr>
            <td>
              {{ ann.authors }}. {{ ann.title }}. <i>{{ ann.magazine }}. {{ ann.year }} {% if ann.issue %}; {{ann.issue}} {% endif %} {% if ann.volume %}({{ ann.volume }}) {% endif %}{% if ann.page_range %}: {{ ann.page_range }}{% endif %}</i>
            </td>
            <td>
              {% if ann.pfile_file_name %}
                <span class="label label-success">
                  <a href="{{ site.baseurl }}/assets/publications/announcements/{{ ann.pfile_file_name }}">Λήψη</a>
                </span>
              {% endif %}
            </td>
          </tr>
        {% endfor %}
      </table> 
    <br>
    <h2><em>ΕΛΛΗΝΙΚΑ ΣΥΝΕΔΡΙΑ</em></h2>
      <table class="table table-striped">
        {% for ann in site.data.greek_announcements %}
          <tr>
            <td>
              {{ ann.authors }}. {{ ann.title }}. <i>{{ ann.magazine }}. {{ ann.year }} {% if ann.issue %}; {{ann.issue}} {% endif %} {% if ann.volume %}({{ ann.volume }}) {% endif %}{% if ann.page_range %}: {{ ann.page_range }}{% endif %}</i>
            </td>
            <td>
              {% if ann.pfile_file_name %}
                <span class="label label-success">
                  <a href="{{ site.baseurl }}/assets/publications/announcements/{{ ann.pfile_file_name }}">Λήψη</a>
                </span>
              {% endif %}
            </td>
          </tr>
        {% endfor %}
      </table>
    <br>
  </div>
</div>
