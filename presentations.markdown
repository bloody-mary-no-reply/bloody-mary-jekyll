---
layout: home
---

<div class="container">

  {% include page-header.html title="ΠΑΡΟΥΣΙΑΣΕΙΣ" %}

  <div class="article">
    <h2>Παρουσιάσεις</h2>
    <h2><em>Παρουσιάσεις Περιστατικών</em></h2>
      <table class="table table-striped">
        {% for case in site.data.case_reports %}
          <tr>
            <td>
              {{ case.authors }}. {{ case.title }}. <i> {{ case.magazine }}. {{ case.year }} </i>
            </td>
            <td>
              <span class="label label-success">
                <a href="{{ site.baseurl}}/assets/publications/case-reports/{{ case.pfile_file_name }}">Λήψη</a>
              </span>
            </td>
          </tr>
        {% endfor %}
</table> 
  

  </div>


</div>
