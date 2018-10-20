# First-one
Hello world repository

<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>JS Bin</title>
</head>
<body>
  <div id="temperatureRegulator">
  <button id="hot" onclick="warmer()">Warmer</button>
  <button id="cold" onclick="colder()">Colder</button><br><br>
  
  <h3 id="currentTemp">Current temperature:</h3>
  <p id="alerts">My favorite temperature is</p>
  <input id="temterature" type="text" value=73></input>
  </div>
</body>
</html>

#temperatureRegulator{
  background-color: grey;
  border-radius: 15px;
  padding: 20px;
  width: 130px;
}

#hot{
  width:60px;
}
#cold{
  padding-left:5px;
  width:60px;
}
#temterature{
  height:50px;
  width:70px;
  position:relative;
  font-size: 25px;
  text-align:center;
  background-color: lightblue;
  margin-left:30px;
}
#currentTemp{
  text-align:center;
}

'use strict';
function warmer(){
	let text;
  let curTemp = document.getElementById('temterature');
  curTemp.value++;
  document.getElementById('temterature').innerHTML = 
  curTemp;
 let ac = curTemp.value;
  if (ac >= 74 && ac < 76){
      text ="Getting warmer";
  } else if (ac >= 76 && ac < 80) {
  	text = "Time to turn A/C on";
  }else if (ac>=80) {
  	text = "Call service guy, your a/c is not working";
  }else if(ac>0 && ac<65){
  	text = 'Heater back on!!!';
  }else if(ac>=65 && ac<73){
  	text = 'So close to normal';
  }else if (ac==73){
  	text = 'Time to relax))';
  }
  document.getElementById('alerts').innerHTML = text;
}

function colder() {
	let coldTemp = document.getElementById('temterature');
	coldTemp.value--;
	document.getElementById('temterature').innerHTML =
	 coldTemp;
	 let text;
	 let heater = coldTemp.value;
	 if (heater<9999 && heater>80) {
	 	text = 'A/C back on!!!';
	 }else if(heater<=80 && heater>73){
        text = 'Getting colder';
	 }else if(heater<=73&& heater>71){
	 	text = 'All right';
	 }else if(heater<=71 && heater>65){
	 	text = 'Time to turn heater on';
	 }else if (heater<=65){
	   text = 'Call service guy, your heater is not working';
	 }
  document.getElementById('alerts').innerHTML = text;
 }


