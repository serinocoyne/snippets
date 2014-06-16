clearfix
========
.clearfix:before,
.clearfix:after {
    content: " ";
    display: table;}

.clearfix:after {
    clear: both;}

.clearfix {
    *zoom: 1;}
    
embed container
==============
.embed-container {
    position: relative;
    padding-bottom: 50%; /* 16/9 ratio */
    padding-top: 30px; /* IE6 workaround*/
    height: 0;
    overflow: hidden;}

.embed-container iframe,
.embed-container object,
.embed-container embed {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height:100%;}
    
jquery
======
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.8.0/jquery.min.js" type="text/javascript"></script>

analytics
=========
<script type="text/javascript">

  var _gaq = _gaq || [];
  _gaq.push(['_setAccount', 'XXXX']);
  _gaq.push(['_trackPageview']);

  (function() {
    var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
    ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
    var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
  })();

</script>

event tracking
==============
ga('send', 'event', 'Tickets', 'Click', 'label');

C5 Snippets
===========
<?php $a = new Area('Content'); $a->display($c); ?>
<?php Loader::element('header_required'); ?>
<?php Loader::element('header_required'); ?>
<?php Loader::element('links'); ?>
<?=$this->getThemePath()?>/

C5 Attributes
=============
replace_link_with_first_in_nav

AJAX Mailing List Submit
========================
$(function () {
    $('#subForm').submit(function (e) {
        e.preventDefault();
        $.getJSON(
        this.action + "?callback=?",
        $(this).serialize(),
        function (data) {
            if (data.Status === 400) {
                alert("Error: " + data.Message);
            } else { // 200
                alert("Success: " + data.Message);
            }
        });
    });
});

meta
====
<meta name="viewport" content="width=device-width">
<meta property="og:title" content="title" />
<meta property="og:description" content="description" />
<meta property="og:image" content="thumbnail_image" />
