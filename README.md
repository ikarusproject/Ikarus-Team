# Ikarus-Team
Nasa Space Challenge
<!DOCTYPE html>
<!-- ikarusnot.html -->
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Ikarusnot Application</title>
 <script>
    var flightnumber = prompt("Enter your flight Number and the departure date: ", "" onclick="javascript:NewCssCal ('demo2','ddMMyyyy')");
    if (confirm("Your flight Number is " + flightnumber)) {
       document.write("<h1>and is scheduled to depart from , " + departureAirportCode + "!</h1>");
    } else {
       document.write("<h1>Please try again.</h1>");
    }
  </script>
   <script>
  var callbackFunction = function(data) {
    var wind = data.query.results.channel.wind;
    alert(wind.chill);
  };
</script>
  // API https://www.air-port-codes.com/airport-codes-api/kati to change airport codes into location so that yahoo weather forecast API uses the location to output weather conditions
<script src="https://query.yahooapis.com/v1/public/yql?q=select wind from weather.forecast where woeid in (select woeid from geo.places(1) where text=location, il')&format=json&callback=callbackFunction"></script>
  //https://developer.yahoo.com/weather/documentation.html#codes make a table with weather condition codes to use in if
  if (code == 0 or 1 or 2 or 3 or 4 or 20 or 23 or 24 or 37 or 38 or 39 or 41 or 43 or 47) {
    document.write("<h1>Your flight is most likely to delay due to bad weather conditions, " + departureAirportCode + "!</h1>");
} else {
    document.write("<h1>Your flight is most likely to be on time, " + departureAirportCode + "!</h1>");
}
</head>
<body>
  <p>Ikarusnot</p>
</body>
</html>
