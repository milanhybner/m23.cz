---
title: Seznam jednot župy Barákovy
layout: default
---

<div id="map1" style="width: 100%; height: 300px;"></div>

<script type="text/javascript">
  var locations1 = [
['http://www.sokol.eu/jednota/20', 50.1832381, 14.6653214, 'Brandýs nad Labem'],
['http://www.sokol.eu/jednota/21', 50.3123372, 14.6175283, 'Byšice'],
['http://www.sokol.eu/jednota/22', 50.3709278, 14.4042803, 'Cítov'],
['http://www.sokol.eu/jednota/23', 50.2954614, 14.6180964, 'Čečelice'],
['http://www.sokol.eu/jednota/24', 50.0746528, 14.8576789, 'Český Brod'],
['http://www.sokol.eu/jednota/25', 50.3929664, 14.4482347, 'Dolní Beřkovice'],
['http://www.sokol.eu/jednota/26', 50.2507008, 14.6422472, 'Dřísy'],
['http://www.sokol.eu/jednota/27', 50.4224283, 14.3903517, 'Horní Počaply'],
['http://www.sokol.eu/jednota/28', 50.0988133, 14.9462450, 'Hořany'],
['http://www.sokol.eu/jednota/29', 49.8713628, 14.8040083, 'Chocerady'],
['http://www.sokol.eu/jednota/30', 49.9485067, 14.8493775, 'Konojedy'],
['http://www.sokol.eu/jednota/31', 50.2245789, 14.5841472, 'Kostelec nad Labem'],
['http://www.sokol.eu/jednota/32', 50.2415922, 14.3119394, 'Kralupy nad Vltavou'],
['http://www.sokol.eu/jednota/33', 50.1663239, 14.7165819, 'Lázně Toušeň'],
['http://www.sokol.eu/jednota/34', 50.4217511, 14.4555194, 'Liběchov'],
['http://www.sokol.eu/jednota/35', 50.4592297, 14.6701144, 'Lobeč'],
['http://www.sokol.eu/jednota/36', 50.2024097, 14.8422947, 'Lysá nad Labem'],
['http://www.sokol.eu/jednota/37', 50.3523106, 14.6951100, 'Mělnické Vtelno'],
['http://www.sokol.eu/jednota/38', 50.3539956, 14.4745778, 'Mělník - Pšovka'],
['http://www.sokol.eu/jednota/39', 50.2268981, 14.8886803, 'Milovice'],
['http://www.sokol.eu/jednota/40', 50.1403500, 14.7959117, 'Mochov'],
['http://www.sokol.eu/jednota/41', 50.2026322, 14.5498681, 'Mratín'],
['http://www.sokol.eu/jednota/42', 50.4385367, 14.6332942, 'Mšeno'],
['http://www.sokol.eu/jednota/43', 50.3539956, 14.4745778, 'na Mělníce'],
['http://www.sokol.eu/jednota/44', 50.1292453, 14.7272203, 'Nehvizdy'],
['http://www.sokol.eu/jednota/45', 50.3666203, 14.4683717, 'Ovčáry - Nedomice'],
['http://www.sokol.eu/jednota/46', 50.1070447, 14.9141217, 'Poříčany'],
['http://www.sokol.eu/jednota/47', 50.0572981, 14.8765944, 'Přistoupim'],
['http://www.sokol.eu/jednota/48', 50.2854614, 14.5823036, 'Přívory'],
['http://www.sokol.eu/jednota/49', 49.8747411, 14.6783506, 'Pyšely'],
['http://www.sokol.eu/jednota/50', 50.3642519, 14.6307772, 'Řepín'],
['http://www.sokol.eu/jednota/51', 49.9932369, 14.6600964, 'Říčany a Radošovice'],
['http://www.sokol.eu/jednota/52', 50.1623814, 14.7534650, 'Sedlčánky'],
['http://www.sokol.eu/jednota/53', 49.9489317, 14.6771361, 'Strančice'],
['http://www.sokol.eu/jednota/54', 49.8963953, 14.8454400, 'Stříbrná Skalice'],
['http://www.sokol.eu/jednota/55', 50.1066175, 14.6800436, 'Šestajovice'],
['http://www.sokol.eu/jednota/56', 50.2536728, 14.3796411, 'Úžice'],
['http://www.sokol.eu/jednota/58', 49.9209258, 14.6406614, 'Velké Popovice'],
['http://www.sokol.eu/jednota/59', 50.1674364, 14.4445986, 'Veltěž'],
['http://www.sokol.eu/jednota/60', 50.2703056, 14.3283969, 'Veltrusy'],
['http://www.sokol.eu/jednota/57', 50.3898492, 14.5941272, 'v Nebuželích'],
['http://www.sokol.eu/jednota/61', 50.2026664, 14.4075122, 'Vodochody - Hoštice'],
['http://www.sokol.eu/jednota/62', 50.3176294, 14.3619139, 'Vraňany'],
['http://www.sokol.eu/jednota/63', 50.2873264, 14.3442186, 'Všestudy'],
['http://www.sokol.eu/jednota/64', 50.2828392, 14.5884119, 'Všetaty'],
['http://www.sokol.eu/jednota/65', 49.9315739, 14.7812483, 'Zvánovice'],
  ];
  var map = new google.maps.Map(document.getElementById('map1'), {
    zoom: 8,
    center: new google.maps.LatLng(50.1663, 14.7166),
    mapTypeId: google.maps.MapTypeId.ROADMAP
  });
  var infowindow = new google.maps.InfoWindow();
  var marker, i;
  for (i = 0; i < locations1.length; i++) {  
    marker = new google.maps.Marker({
      position: new google.maps.LatLng(locations1[i][1], locations1[i][2]),
      map: map,
      title: locations1[i][3],
    });
    google.maps.event.addListener(marker, 'click', (function(marker, i) {
      return function() {
        window.open(locations1[i][0]);
        //infowindow.setContent(locations[i][0]);
        //infowindow.open(map, marker);
      }
    })(marker, i));
  }
</script>

Brandýs nad Labem  
Byšice  
Cítov  
Čečelice  
Český Brod  
Dolní Beřkovice  
Dřísy  
Horní Počaply  
Hořany  
Chocerady  
Konojedy  
Kostelec nad Labem  
Kralupy nad Vltavou  
Lázně Toušeň  
Liběchov  
Lobeč  
Lysá nad Labem  
Mělnické Vtelno  
Mělník - Pšovka  
Milovice  
Mochov  
Mratín  
Mšeno  
na Mělníce  
Nehvizdy  
Ovčáry - Nedomice  
Poříčany  
Přistoupim  
Přívory  
Pyšely  
Řepín  
Říčany a Radošovice  
Sedlčánky  
Strančice  
Stříbrná Skalice  
Šestajovice  
Úžice  
Velké Popovice  
Veltěž  
Veltrusy  
v Nebuželích  
Vodochody - Hoštice  
Vraňany  
Všestudy  
Všetaty  
Zvánovice  