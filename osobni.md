---
layout: default
title: Osobní
---

[Akce](#akce) \| [Úkoly](#ukoly) \| [Poznámky](#poznamky)

# Ústřední škola České obce sokolské

<ul>
{% for post in site.us %}<li><a href="{{ post.url | prepend: site.baseurl}}">{{ post.title }}</a></li>{% endfor %}
</ul>

# Župa Barákova

<ul>
{% for post in site.zb %}<li><a href="{{ post.url }}">{{ post.title }}</a></li>{% endfor %}
</ul>

# Sokol Šestajovice

<ul>
{% for post in site.tr %}<li><a href="{{ post.url | prepend: site.baseurl}}">{{ post.title }}</a></li>{% endfor %}
</ul>

---

[![Vize18](vize18.png "Podporuji Vizi 18")](http://www.vize18.cz)

---

<div id="akce">
    <input class="search form-control" placeholder="Akce" type="text">
    <table class="table">
        <tbody class="list">
     {%for akce in site.data.akce %}
            <tr>
                <td class="i" style="width:20%">{{akce.i}}</td>
                <td class="c" style="width:10%">{{akce.c}}</td>
                <td class="t" style="width:70%">
                    <a href="{{akce.u}}">{{akce.t}}</a>
                </td>
            </tr>
    {% endfor %}
        </tbody>
    </table>
    <script type="text/javascript">
        var options = {
          valueNames: ['i', 't', 'c']
      };
      var entryList = new List('akce', options);

    </script>
</div>

<div id="ukoly">
    <input class="search form-control" placeholder="Úkoly" type="text">
    <table class="table">
        <tbody class="list">
     {%for ukol in site.data.ukoly %}
            <tr>
                <td class="i" style="width:20%">{{ukol.i}}</td>
                <td class="c" style="width:10%" >{{ukol.c}}</td>
                <td class="t" style="width:70%">
                    <a href="{{ukol.u}}">{{ukol.t}}</a>
                </td>
            </tr>
             {% endfor %}
        </tbody>
    </table>
    <script type="text/javascript">

    var options = {
    valueNames: ['i', 't', 'c']
    };
    var entryList = new List('ukoly', options);

    </script>
</div>

<div id="poznamky">
    <input class="search form-control" placeholder="Poznámky" type="text">
    <table class="table">
        <tbody class="list">
     {%for poznamka in site.data.poznamky %}
            <tr>
                <td class="i" style="width:20%"><a href="{{poznamka.u}}">{{poznamka.i}}</a></td>
                <td class="c" style="width:10%">{{poznamka.c}}</td>
                <td class="t" style="width:70%">{{poznamka.t}}</td>
            </tr>
             {% endfor %}
        </tbody>
    </table>
    <script type="text/javascript">

    var options = {
    valueNames: ['i', 'c', 't']
    };
    var entryList = new List('poznamky', options);

    </script>
</div>