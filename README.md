# Nigeria vector-map
creating a vector map for Nigeria
created by sanusi korede yusuf
email: sanusikorede@gmail.com

This project is created using jquery vector map (jqvmap) on december 2016. I chose to write this for developer who are out there looking for Nigerian vector maps or wants to integrate it in their application, here is a simple code to help you out.

Your html head section will look like this

<head>
   
    <link href="dist/jqvmap.css" media="screen" rel="stylesheet" type="text/css" />

    <style>
        html, body {
            padding: 0;
            margin: 0;
            width: 100%;
            height: 100%;
        }
        #vmap {
            width: 100%;
            height: 100%;
            background-color: red;
        }
    </style>


    <script type="text/javascript" src="http://code.jquery.com/jquery-1.11.3.min.js"></script>
    <script type="text/javascript" src="dist/jquery.vmap.js"></script>
    <script type="text/javascript" src="dist/maps/jquery.vmap.nigeria.js" charset="utf-8"></script>

    <script>
      jQuery(document).ready(function () {
        jQuery('#vmap').vectorMap({
            map: 'nigeria_ng',
            backgroundColor: '#a5bfdd',
            borderColor: '#818181',
            borderOpacity: 0.25,
            borderWidth: 1,
            color: '#f4f3f0',
            enableZoom: true,
            hoverColor: '#c9dfaf',
            hoverOpacity: null,
            normalizeFunction: 'linear',
            scaleColors: ['#b6d6ff', '#005ace'],
            selectedColor: '#c9dfaf',
            selectedRegions: null,
            showTooltip: true,
            onRegionClick: function (element, code, region) {
                var message = 'You clicked "'
                    + region
                    + '" which has the code: '
                    + code.toUpperCase();
                alert(message);
            }
        });
      });
    </script>

