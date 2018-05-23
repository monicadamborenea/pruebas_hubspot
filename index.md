<!DOCTYPE html> 
<html> 
<head> 
    <title>Home Questionnaire<span id="selection-marker-1" class="redactor-selection-marker"></span></title> 

<script>
!function () { 
var analytics = window.analytics = window.analytics || []; 
if (!analytics.initialize) if (analytics.invoked) window.console && console.error && console.error("Segment snippet included twice."); else { 
analytics.invoked = !0; 
analytics.methods = ["trackSubmit", "trackClick", "trackLink", "trackForm", "pageview", "identify", "reset", "group", "track", "ready", "alias", "page", "once", "off", "on"]; 
analytics.factory = function (t) { 
return function () { 
var e = Array.prototype.slice.call(arguments); 
e.unshift(t); 
analytics.push(e); 
return analytics 
} 
}; 
for (var t = 0; t < analytics.methods.length; t++) { 
var e = analytics.methods[t]; 
analytics[e] = analytics.factory(e) 
} 
analytics.load = function (t) { 
var e = document.createElement("script"); 
e.type = "text/javascript"; 
e.async = !0; 
e.src = ("https:" === document.location.protocol ? "https://" : "http://") + "cdn.segment.com/analytics.js/v1/" + t + "/analytics.min.js"; 
var n = document.getElementsByTagName("script")[0]; 
n.parentNode.insertBefore(e, n) 
}; 
analytics.SNIPPET_VERSION = "3.1.0"; 
var TRAITS = {}, PROPS = {}, integrations = {}, REFERRER;

function getParameterByName(e) { 
e = e.replace(/[\[]/, "\\[").replace(/[\]]/, "\\]"); 
var m = new RegExp("[\\?&]" + e + "=([^&#]*)"), t = m.exec(location.search); 
return null === t ? "" : decodeURIComponent(t[1].replace(/\+/g, " ")) 
}

document.referrer && (REFERRER = document.referrer); 
var utm_source = getParameterByName("utm_source"), utm_medium = getParameterByName("utm_medium"), 
utm_term = getParameterByName("utm_term"), utm_content = getParameterByName("utm_content"), 
utm_campaign = getParameterByName("utm_campaign"), gclid = getParameterByName("gclid"); 
"" !== utm_source && (PROPS.utm_source = utm_source), "" !== utm_medium && (PROPS.utm_medium = utm_medium), "" !== utm_term && (PROPS.utm_term = utm_term), "" !== utm_content && (PROPS.utm_content = utm_content), "" !== utm_campaign && (PROPS.utm_campaign = utm_campaign), "" !== gclid && (PROPS.gclid = gclid);

analytics.load("ywhUp6VsHaahiJssv7f0jn661boN84jv"); 

integrations.Intercom = { 
user_hash: "008f5f775e112a0f322bcfbba1611c8a2f41b7e3f992476678b1ac2396994898", 
}; 
TRAITS.email = "greg.hinch.testmay21@growthstreet.co.uk"; // Email address 
TRAITS.createdAt = "1526923350"; // Signup date as a Unix timestamp 
TRAITS.is_lender = true; 
analytics.identify("greg.hinch.testmay21@growthstreet.co.uk", TRAITS, integrations); 
analytics.page({properties: PROPS, referrer: REFERRER}) 
} 
}();

</script>
    


    
    
</head> 
<body> 
<h1>What is your favorite place to travel?</h1> 
<p>I am building a directory of the sweetest travel destinations.</p>  
<form name="travel" onsubmit="identify(event)">
     What is your favorite travel destination?
    <input name="destination" required="" size="81" type="text"/> 
    <br><br><br> 
    Any recommendations (cool things to do, places to visit or restaurants to eat)? 
    <br><br> 
    <textarea cols="81" name="details" required="" rows="10">
    </textarea> 
    <br><br> 
    Name: <input name="fullname" required="" size="75" type="text"/> 
    <br><br> 
    Email: <input name="email" required="" size="75" type="email"/> 
    <br><br>
    <input name="submit" type="submit" value="submit"/>
</form> 
    <script type="text/javascript">
      function identify(e){
        e.preventDefault();
        var form = e.target;
        var email = form["email"].value;
        var fullname = form["fullname"].value;
        var destination = form["destination"].value;
        var details = form["details"].value;
        var user = {
            email: email, 
            name: fullname, 
            destination: destination, 
            details: details
        };
        analytics.identify(12345, {
            email: email, 
            name: fullname
        });
        analytics.track('destination submitted', user, function() {
            window.location.href = "";
        });
      }
</script>
</body> 
</html>
