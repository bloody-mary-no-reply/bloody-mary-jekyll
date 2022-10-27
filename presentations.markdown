---
layout: home
---

<div class="container">

  {% include page-header.html title="ΠΑΡΟΥΣΙΑΣΕΙΣ" %}

  <div class="article">
    <h2>Παρουσιάσεις</h2>
    <h2><em>Ομιλίες</em></h2>
      <table class="table table-striped">
        {% for talk in site.data.talks %}
          <tr>
            <td>
              {{ talk.authors }}. {{ talk.title }}. <i>{{ talk.magazine }}. {{ talk.year }}</i>
            </td>
            <td>
              {% if talk.pfile_file_name %}
                <span class="label label-success">
                  <a href="{{ site.baseurl }}/assets/publications/talks/{{ talk.pfile_file_name }}">Λήψη</a>
                </span>
              {% endif %}
            </td>
          </tr>
        {% endfor %}
      </table> 
    <br>
    <h2><em>Ανασκοπήσεις</em></h2>
      <table class="table table-striped">
        {% for review in site.data.reviews %}
          <tr>
            <td>
              {{ review.authors }}. {{ review.title }}. <i>{{ review.magazine }}. {{ review.year }}</i>
            </td>
            <td>
              {% if review.pfile_file_name %}
                <span class="label label-success">
                  <a href="{{ site.baseurl }}/assets/publications/reviews/{{ review.pfile_file_name }}">Λήψη</a>
                </span>
              {% endif %}
            </td>
          </tr>
        {% endfor %}
      </table> 
    <br>
    <h2><em>Βιβλιογραφικές Ενημερώσεις</em></h2>
      <table class="table table-striped">
        {% for biblio in site.data.bibliographies %}
          <tr>
            <td>
              {{ biblio.authors }}. {{ biblio.title }}. <i>{{ biblio.magazine }}. {{ biblio.year }}</i>
            </td>
            <td>
              {% if biblio.pfile_file_name %}
                <span class="label label-success">
                  <a href="{{ site.baseurl }}/assets/publications/bibliographies/{{ biblio.pfile_file_name }}">Λήψη</a>
                </span>
              {% endif %}
            </td>
          </tr>
        {% endfor %}
      </table> 
    <br>
    <h2><em>Παρουσιάσεις Περιστατικών</em></h2>
      <table class="table table-striped">
        {% for case in site.data.case_reports %}
          <tr>
            <td>
              {{ case.authors }}. {{ case.title }}. <i>{{ case.magazine }}. {{ case.year }}</i>
            </td>
            <td>
              <span class="label label-success">
                <a href="{{ site.baseurl }}/assets/publications/case-reports/{{ case.pfile_file_name }}">Λήψη</a>
              </span>
            </td>
          </tr>
        {% endfor %}
      </table> 
  </div>
</div>
