---
layout: home
title: Home
landing-title: "Hi, I'm The Joey!"
description: null
image: null
author: null
show_tile: false
---
<script>
    var thoughts = [{% for thought in site.data.deepthoughts %}
        `{{ thought | escape | strip }}`{% unless forloop.last %},{% endunless %}{% endfor %}
    ];
    var selection = parseInt(Math.random() * thoughts.length);
    document.write(thoughts[selection]);
</script>
