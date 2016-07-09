---
layout: default
title: osobní
---

<div class="cal">
    <input class="search" placeholder="Filtrovat" type="text">
    <table>
        <thead>
            <tr>
                <th style="width: 20%">Datum</th>
                <th></th>
                <th style="width: 60%">Název</th>
            </tr>
        </thead>
        <tbody class="list">
            {%for akce in site.data.cal %}
            <tr>
                <td class="datum">{{akce.datum}}</td>
                <td class="kontext">{{akce.kontext}}</td>
                <td class="nazev">
                    <a href="{{akce.url}}">{{akce.nazev}}</a>
                </td>
            </tr>
            {% endfor %}
        </tbody>
    </table>
    <script type="text/javascript">

        var options = {
          valueNames: ['datum', 'nazev', 'kontext']
      };
      var entryList = new List('cal', options);

</div>


</script>

<script type="text/javascript">

var options = {
  valueNames: ['datum', 'nazev', 'druh']
};
var entryList = new List('entry-list', options);

</script>
<script type="text/javascript">

var options = {
  valueNames: ['datum', 'nazev', 'druh']
};
var entryList = new List('entry-list', options);

</script>