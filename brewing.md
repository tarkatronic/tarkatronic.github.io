---
title: Brewing
layout: post
nav-menu: true
image: assets/images/brewing.jpg
---
Since my daughter was born, my wife and I have found ourselves spending a lot
more time at home, and in need of things to keep us occupied. Given our long
time love of beer, brewing seemed like a natural new hobby for us to take on!
And it sure has been a fun one.

Here are some of the things we have brewed:
<div class="row">
    <table class="alt">
        {% for brew in site.data.brewing %}
        <tr>
            <td>
                <span class="image left brew">
                {% if brew.image %}<img src="{{ site.baseurl }}/{{ brew.image }}" alt="{{ brew.name }}">{% else %}
                <span><img src="{{ site.baseurl }}/assets/images/brewing/default_beer.png" alt="{{ brew.name }}"></span>{% endif %}
                </span>
                <strong>{{ brew.name }}</strong><br>
                <strong>Style:</strong> {{ brew.style }}<br>
                <strong>Approx ABV:</strong> {{ brew.abv }}<br>
                {% if brew.description %}<strong>Description:</strong> {{ brew.description | newline_to_br }}<br>{% endif %}
                <br><a href="{{ brew.link }}">Batch Notes on Brewfather</a>
            </td>
        </tr>{% endfor %}
    </table>
</div>
