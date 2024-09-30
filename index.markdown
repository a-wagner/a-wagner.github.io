---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

![Andrew Wagner](assets/pic.png){:class="resp-img"}{:height="auto"}{:width="200"}{:style="border-radius:50%"}


I'm a PhD student studying programming languages with 
[Amal Ahmed][amal] in the [Programming Research Laboratory][prl] at [Northeastern University][khoury].
Previously, I graduated from [Brown University][brown], 
where I was advised by [Shriram Krishnamurthi][shriram] and [Tim Nelson][tim].
I'm broadly interested in language-based security with an eye toward language interoperability and cryptography.
{:style="text-align: justify"}

**email:** ahwagner at ccs.neu.edu  
**pronouns:** he/him/his

<br style="clear: both">

<a id="pubs"></a>
## Papers

{% for pub in site.data.pubs %}
  - **{{ pub.title }}**  
    {{ pub.authors }}  
    *{{ pub.venue }}*  
    <div>
    {% for link in pub.links %}
      <a href="{{ link.url }}" target="_blank">{{ link.name }}</a>
      {% unless forloop.last %} | {% endunless %}
    {% endfor %}
    </div>
{% endfor %}

<a id="talks"></a>
## Talks 

{% for talk in site.data.talks %}
  - **{{ talk.title }}**  
    {{ talk.venue }}  
    <div>
    {% for link in talk.links %}
      <a href="{{ link.url }}" target="_blank">{{ link.name }}</a>
      {% unless forloop.last %} | {% endunless %}
    {% endfor %}
    </div>
{% endfor %}

<a id="service"></a>
## Academic Service

{% for service in site.data.service %}
  - **{{ service.venue }}:** {{ service.role }}  
    <div></div>
{% endfor %}

<a id="teaching"></a>
## Teaching
{% for course in site.data.teach %}
  - **{{ course.course }}**, {{ course.where }}  
    <div>
    {% for role in course.roles %}
      {{ role.role }} ({{ role.when | join: ", " }})
      {% unless forloop.last %} , {% endunless %}
    {% endfor %}
    </div>
{% endfor %}

[amal]: https://ccs.neu.edu/~amal/
[khoury]: https://www.khoury.northeastern.edu/
[prl]: https://prl.khoury.northeastern.edu/
[brown]: https://cs.brown.edu/
[shriram]: https://cs.brown.edu/~sk/
[tim]: https://cs.brown.edu/people/tbn/
