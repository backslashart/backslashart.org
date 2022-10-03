---
title: \Art at Cornell Tech
description: Pronounced “backslash art”, \Art supports bleeding edge technological interventions into artistic practice.
---
## > TOP
{% assign a = 0 %}
{% assign ip = 0 %}

{% assign awards = site.awards | sort:"year" | reverse %}
{% for award in awards %}
{% assign artist = site.artists | where: "year",award.year | first %}
{% assign fellows = site.fellows | where: "year",award.year | sort:"name" %}
{% if fellows.size == 2 %}
{% assign authors = artist.name | append: ", " | append: fellows[0].name | append: ", and " | append: fellows[1].name %} 
{% else %}
{% assign authors = artist.name | append: " and " | append: fellows[0].name %} 
{% endif %}

{% if award.is-complete %}
{% assign c = a | minus: ip %}
## > [{{ award.art-title | upcase }} \ART AWARD {{ award.year }}]( {{ award.url }} )
{{ authors }}
<p class="banner"><a href="{{ award.url }}"><img src="{{ award.banner }}"></a></p>
{{ award.description }} <a href="{{ award.url }}">More about {{ award.art-title }}</a>.
{% else %}
{% assign ip = ip | plus: 1 %}
{% if ip == 1 %}
{% endif %}
\Art {{ award.year }} with {{ authors }} coming soon{% if a >= 1 %}er{% endif %}!
{% endif %}

{% if c == 0 %}
## > <a name="about"></a>ABOUT \ART
\Art, pronounced “backslash art”, supports bleeding edge technological interventions into artistic practice.

\Art lives at [Cornell Tech](http://tech.cornell.edu/){:target="_blank"}, a digital-age, technology-forward graduate campus of Cornell University in New York City. \Art collides students, faculty, and artists, both on and off campus, providing <a href="#award">awards</a> and <a href="#microgrants">grants</a> for art works, art tools, and art activities that engage the latest emerging digital technologies.
{% endif %}

{% if c == 1 %}
## > <a name="award"></a>ABOUT THE \ART AWARD
\Art awards a major $100k grant each year to a practicing NYC-based artist and two Cornell Tech graduates to collaborate full-time on a significant work of art that uses bleeding edge digital technology to provoke novel opportunities for their work.

For the artist, this award offers sustained access to significant engineering capability, enabling deep exploration of new forms, expressions, and features for their work. For the Cornell Tech graduates, the award is an opportunity to flex creatively after graduation, absorb a distinct mode of cultural practice, and take an uncommon path.

Check out past \Art awards ({% for awrd in awards %}{% if awrd.is-complete %}{% if not-first-awrd %}, {% endif %}[{{ awrd.year }}]({{ awrd.url }}){% assign not-first-awrd = "true" %}{% endif %}{% endfor %}); and read more about the [\Art award process](/award/).
{% endif %}

{% assign a = a | plus: 1 %}
{% endfor %}

## > <a name="microgrants"></a>ABOUT \ART MICROGRANTS
\Art awards $500 Microgrants on a rolling basis to assist current Cornell University students pursuing art works, art tools, or other art activities that use emerging digital technologies. Read more about [\Art Microgrants](/microgrants/).

## > ABOUT THE \
Backslash (\\), otherwise known as whack, hack, slosh, bash, backslant, and reversed virgule\-\-and not to be confused with forward slash (/)\-\-is known as an escape character in computer programming, indicating that the characters after the \ should be interpreted outside the normal mode of input and output to do something special. 

## > WHOIS \ART
\Art is a mix of Cornell Tech & Cornell University faculty & staff and practitioners with technology and art expertise: Justin Bakse (Director), Greg Pass (Founder), Andrea Inselmann, Zachary Kaplan, J McLoughlin, Alap Parikh, Brandon Plaster, Noah Snavely, and Matthew Weinstein.

<div id="about-CT" markdown="1">
## > ABOUT CORNELL TECH
Cornell Tech is a new graduate campus of Cornell University located on Roosevelt Island in New York City. It brings together faculty, business leaders, tech entrepreneurs, and students in a catalytic environment to produce visionary results grounded in significant needs that will reinvent the way we live in the digital age. Read more about [Cornell Tech](https://tech.cornell.edu){:target="_blank"}.
<div id="CT-logo"></div>
</div>

{% include newsletter.html %}

## > CONTACT
For questions, press, and other inquiries, please email info @ backslashart.org.
