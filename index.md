---
title: \Art at Cornell Tech
description: Pronounced “backslash art”, \Art supports bleeding edge technological interventions into artistic practice.
---

{% assign a = 0 %}

{% assign awards = site.awards | sort:"year" | reverse %}
{% for award in awards %}
{% assign artist = site.artists | where: "year",award.year | first %}
{% assign fellows = site.fellows | where: "year",award.year | sort:"name" %}
{% if fellows.size == 2 %}
{% assign authors = artist.name | append: ", " | append: fellows[0].name | append: ", and " | append: fellows[1].name %}
{% elsif fellows.size == 1 %}
{% assign authors = artist.name | append: " and " | append: fellows[0].name %}
{% else %}
{% assign authors = artist.name %}
{% endif %}

{% if award.is-complete %}

## > [{{ award.art-title | upcase }} \ART {{ award.year }}]( {{ award.url }} )

{{ authors }}

<p class="banner"><a href="{{ award.url }}"><img src="{{ award.banner }}"></a></p>
{{ award.description }} <a href="{{ award.url }}">More about {{ award.art-title }}</a>.

{% else %}
## > \ART {{ award.year }}
\Art with {{ authors }} in progress!
{% endif %}

{% if a == 2 %}

## > <a name="about"></a>ABOUT \ART

\Art, pronounced “backslash art”, funds far-out works of art and technology. 

\Art lives at [Cornell Tech](http://tech.cornell.edu/){:target="\_blank"}, a digital-age, technology-forward graduate campus of Cornell University in New York City. \Art collides students, faculty, and artists, both on and off campus, providing grants for works of art and technology that are uniquely unconventional.
{% endif %}

{% if c == 4 %}

## > <a name="award"></a>ABOUT THE \ART FELLOWSHIP

Starting in 2023, \Art awards a fellowship to a visiting artist to collaborate with Cornell Tech faculty and students on a significant work of art that engages bleeding edge digital research and technology. The fellowship offers sustained teamwork with creative and innovative technologists, enabling deep exploration of new artistic forms, expressions and features, and is intended to provoke novel opportunities for the artist’s work.

## > ABOUT THE \ART AWARD

From 2016 to 2022, \Art awarded a major grant each year to a practicing NYC-based artist and one or two Cornell Tech graduates to collaborate full-time on a significant work of art that used bleeding edge digital technology.

Check out past \Art Awards: {% for awrd in awards %}{% if awrd.is-complete %}{% if not-first-awrd %}, {% endif %}[{{ awrd.year }}]({{ awrd.url }}){% assign not-first-awrd = "true" %}{% endif %}{% endfor %}.
{% endif %}

{% assign a = a | plus: 1 %}
{% endfor %}

## > <a name="microgrants"></a>ABOUT \ART MICROGRANTS

\Art awards $500 Microgrants on a rolling basis to assist current Cornell University students pursuing art works, art tools, or other art activities that use emerging digital technologies. Read more about [\Art Microgrants](/microgrants/).

## > ABOUT THE \

Backslash (\\), otherwise known as whack, hack, slosh, bash, backslant, and reversed virgule\-\-and not to be confused with forward slash (/)\-\-is known as an escape character in computer programming, indicating that the characters after the \ should be interpreted outside the normal mode of input and output to do something special.

<div id="about-CT" markdown="1">
## > ABOUT CORNELL TECH
Cornell Tech is a new graduate campus of Cornell University located on Roosevelt Island in New York City. It brings together faculty, business leaders, tech entrepreneurs, and students in a catalytic environment to produce visionary results grounded in significant needs that will reinvent the way we live in the digital age. Read more about [Cornell Tech](https://tech.cornell.edu){:target="_blank"}.
<div id="CT-logo"></div>
</div>

{% include newsletter.html %}

## > CONTACT

For questions, press, and other inquiries, please email info @ backslashart.org.
