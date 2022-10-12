---
layout: home
---

 {::comment} this page is supposed to handle both all posts and specific categories {:/comment}
<div class="container">

  {% include page-header.html title="Άρθρα" %}

  <h2>Άρθρα</h2>
    <div class="row">
      <div class="col-md-12">
        <div class="blog-posts">
          <section class="timeline">
            <div class="timeline-body">
              {% for post in site.posts %}
                  {% assign currentdate = post.date | date: "%Y %B" %}
                    {% if currentdate != date %}
                      <div class="timeline-date">
                        <h3 class="heading-primary">{{currentdate}}</h3>
                      </div>
                      {% assign date = currentdate %}
                   {% endif %}
                   <article class="{% cycle 'timeline-box left post post-medium', 'timeline-box right post post-medium' %}">
                     <div class="row">
                       <div class="col-md-12">
                         <div class="post-image">
                           <div class="owl-carousel owl-theme" data-plugin-options='{"items":1}'>
                             <div>
                               <div class="img-thumbnail">
                                 {% capture imagename %}{% cycle 'assets/img/md91.jpg', 'assets/img/md81.JPG', 'assets/img/md4.jpg' %}{% endcapture %}
                                 <img src="{{ imagename | relative_url }}" class="img-responsive" />
                               </div>
                             </div>
                           </div>
                         </div>
                       </div>
                     </div>
                     <div class="row">
                       <div class="col-md-12">
                         <div class="post-content">
                           <h4 class="heading-primary">{{ post.title }}</h4>
                           <p>{{ post.content | split:'<!--break-->' | first  | markdownify }}...</p>
                         </div>
                       </div>
                     </div>
                     <div class="row">
                       <div class="col-md-12">
                         <div class="post-meta">
                           <span><i class="fa fa-calendar"></i>  {{ post.date | date: "%d-%m-%Y" }}  </span><br>
                         </div>
                       </div>
                     </div>
                     <div class="row">
                       <div class="col-md-12">
                         <div class="post-meta">
                           <span><i class="fa fa-user"></i> από {{ post.author }} </span>
                           <span><i class="fa fa-tag"></i> κατηγορία: {{ post.categories | first }} </span>
                           <!--<span><i class="fa fa-comments"></i> <a href="#">12 Comments</a></span>-->
                         </div>
                       </div>
                     </div>
                     <div class="row">
                       <div class="col-md-12">
                         <a href="{{site.baseurl}}{{ post.url }}" class='btn btn-xs btn-primary pull-right'>Διαβάστε </a>
                       </div>
                     </div>
                   </article>
              {% endfor %}
            </div>
          </section>
        </div>
      </div>
    </div>
</div>


