// ==UserScript==
// @name          .:*~-ł‗Ĉ‗É‗Μ‗Ǿ‗Ď-~*:.
// @namespace   -
// @version      Lastest_Version
// @description  ł‗Ĉ‗É Ǿ‗ņ м‗¥ √‗ⓔ‗¡‗Ņ‗š
// @author       K + Jack L㊊L
// ---------------------------------------------------------------------------______--------_
// @match        *://moomoo.io/*
// @match        *://sandbox.moomoo.io/*
// @match        *://dev.moomoo.io/*
// @match        *://mm_beta.moomoo.io/*
// @require https://greasyfork.org/scripts/368273-msgpack/code/msgpack.js?version=598723
// @require http://code.jquery.com/jquery-3.3.1.min.js
// @require https://code.jquery.com/ui/1.12.0/jquery-ui.min.js
// @require https://cdnjs.cloudflare.com/ajax/libs/jquery-confirm/3.3.0/jquery-confirm.min.js
// ==/UserScript==
var ID_WinterCap = 15;
var ID_FlipperHat = 31;
var ID_MarksmanCap = 1;
var ID_BushGear = 10;
var ID_SoldierHelmet = 6;
var ID_AntiVenomGear = 23;
var ID_MusketeerHat = 32;
var ID_MedicGear = 13;
var ID_BullHelmet = 7;
var ID_EmpHelmet = 22;
var ID_BoosterHat = 12;
var ID_BarbarianArmor = 26;
var ID_BullMask = 46;
var ID_WindmillHat = 14;
var ID_SpikeGear = 11;
var ID_BushidoArmor = 16;
var ID_SamuraiArmor = 20;
var ID_ScavengerGear = 27;
var ID_TankGear = 40;
var ID_TurretGear = 53;
var ID_Pig = 29;

// Keys
var TankGearKey = 90;
var BullHelmetKey = 74;
var SoldierHelmetKey = 71;
var TurretKey = 72;
var BoosterHatKey = 66;
var Pig = 12; // Too Cute
var uneqiup = 16;
var SpikeGearKey = 89;
var EmpKey = 84;
var SamuKey = 80;
var SpikeKey = 86;
var PitKey = 70;
var PikeKey = 86;
var WindKey = 78;
try {
    document.getElementById("moomooio_728x90_home").style.display = "none";
    $("moomooio728x90_home").parent().css({display: "none"});
} catch (e) {
    console.log("There was an error removing the ads.");
}


var menuChange = document.createElement("div");
menuChange.className = "menuCard";
menuChange.id = "mainSettings";
menuChange.innerHTML = `
<div id="simpleModal" class="modal">
    <div class="modal-content">
        <div class="modal-header">
            <span class="closeBtn">&times;</span>
            <h2 style="font-size: 17px;">MooJax & Macro Settings</h2>
        </div>
        <div class="modal-body" style="font-size: 17px;">
            <div class="flexControl">
                <h3 style="color: #000; font-size: 17px;">To unquip a hat press: LEFT SHIFT</h3>
                <h3 style="color: #000; font-size: 17px;">To unquip a acc press: THE "<" KEY</h3>
                <br><h3 class="menuPrompt">Tank Gear: </h3> <input value="${String.fromCharCode(TankGearKey)}" id="tankGear" class="keyPressLow" onkeyup="this.value = this.value.toUpperCase();" maxlength="1" type="text"/>
                <h3 class="menuPrompt">Bull Helmet: </h3> <input value="${String.fromCharCode(BullHelmetKey)}" id="bullHelm" class="keyPressLow" onkeyup="this.value = this.value.toUpperCase();" maxlength="1" type="text"/><br>
                <br><h3 class="menuPrompt">Soldier Helmet: </h3> <input value="${String.fromCharCode(SoldierHelmetKey)}" id="soldier" class="keyPressLow"onkeyup="this.value = this.value.toUpperCase();"  maxlength="1" type="text"/>
                <h3 class="menuPrompt">Turret Gear: </h3> <input value="${String.fromCharCode(TurretKey)}" id="turret" class="keyPressLow" maxlength="1" onkeyup="this.value = this.value.toUpperCase();" type="text"/><br>
                <br><h3 class="menuPrompt">Booster Hat: </h3> <input value="${String.fromCharCode(BoosterHatKey)}" id="booster" class="keyPressLow" maxlength="1" onkeyup="this.value = this.value.toUpperCase();" type="text"/>
                <h3 class="menuPrompt">Spike Gear: </h3> <input value="${String.fromCharCode(SpikeGearKey)}" id="spikeg" class="keyPressLow" maxlength="1" onkeyup="this.value = this.value.toUpperCase();" type="text"/><br>
                <br><h3 class="menuPrompt">Emp Helmet: </h3> <input value="${String.fromCharCode(EmpKey)}" id="emp" class="keyPressLow" onkeyup="this.value = this.value.toUpperCase();" maxlength="1" type="text"/>
                <h3 class="menuPrompt">Samurai Armor:</h3> <input value="${String.fromCharCode(SamuKey)}" id="samu" class="keyPressLow" onkeyup="this.value = this.value.toUpperCase();" maxlength="1" type="text"/><br>
                <h3 class="menuPrompt">Pig Head:</h3> <input value="${String.fromCharCode(Pig)}" id="pigh" class="keyPressLow" onkeyup="this.value = this.value.toUpperCase();" maxlength="1" type="text"/><br>
                <h3 style="color: #000; font-size: 17px;">Wings + Hat Combo:</h3>
                <h3 class="menuPrompt">Acc:</h3> <input value="${String.fromCharCode(0)}" id="ACCONE" class="keyPressLow" onkeyup="this.value = this.value.toUpperCase();" maxlength="2" type="number"/><br>
                <h3 class="menuPrompt">Hat:</h3> <input value="${String.fromCharCode(0)}" id="HATONE" class="keyPressLow" onkeyup="this.value = this.value.toUpperCase();" maxlength="2" type="number"/><br>
                <h3 style="font-size: 17px;"> Settings </h3>
                <label class="container">Show biomes on the map ?(Snow, Plains, desert)
                    <input type="checkbox" id="myCheck">
                    <span class="checkmark"></span>
                </label>
                <div>
                </div>
                <label class="container">Put pike on the InstaKill?
                    <input type="checkbox" id="myCheck2">
                    <span class="checkmark"></span>
                </label>
                <label class="container">Enable Hat Macro?
                    <input type="checkbox" id="myCheck3">
                    <span class="checkmark"></span>
                </label>
            </div>
        </div>
        <div class="modal-footer">
            <h3 style="font-size: 17px;">Edit and live save your changes !</h3>
            <p>Sub to (JackLaL)</p>
        </div>
    </div>
</div>
`
document.body.appendChild(menuChange)
$("#tankGear").on("input", () => {
    var cval = $("#tankGear").val();
    if (cval){
        TankGearKey = cval.toUpperCase();
        TankGearKey = TankGearKey.charCodeAt(0);
        console.log(TankGearKey);
    }
});
$("#pigh").on("input", () => {
    var cval = $("#pigh").val();
    if (cval){
        Pig = cval.toUpperCase();
        Pig = Pig.charCodeAt(0);
        console.log(Pig);
    }
});

$("#bullHelm").on("input", () => {
    var cval = $("#bullHelm").val();
    if (cval){
        BullHelmetKey = cval.toUpperCase();
        BullHelmetKey = BullHelmetKey.charCodeAt(0);
        console.log(BullHelmetKey);
    }
});

$("#soldier").on("input", () => {
    var cval = $("#soldier").val();
    if (cval){
        SoldierHelmetKey = cval.toUpperCase();
        SoldierHelmetKey = SoldierHelmetKey.charCodeAt(0);
        console.log(SoldierHelmetKey);
    }
});

$("#turret").on("input", () => {
    var cval = $("#turret").val();
    if (cval){
        TurretKey = cval.toUpperCase();
        TurretKey = TurretKey.charCodeAt(0);
        console.log(TurretKey);
    }
});



$("#emp").on("input", () => {
    var cval = $("#emp").val();
    if (cval){
        EmpKey = cval.toUpperCase();
        EmpKey = EmpKey.charCodeAt(0);
        console.log(EmpKey);
    }
});

$("#samu").on("input", () => {
    var cval = $("#samu").val();
    if (cval){
        SamuKey = cval.toUpperCase();
        SamuKey = SamuKey.charCodeAt(0);
        console.log(SamuKey);
    }
});
$("#booster").on("input", () => {
    var cval = $("#booster").val();
    if (cval){
        BoosterHatKey = cval.toUpperCase();
        BoosterHatKey = BoosterHatKey.charCodeAt(0);
        console.log(BoosterHatKey);
    }
});

$("#spikeg").on("input", () => {
    var cval = $("#spikeg").val();
    if (cval){
        SpikeGearKey = cval.toUpperCase();
        SpikeGearKey = SpikeGearKey.charCodeAt(0);
        console.log(SpikeGearKey);
    }
});

$("#trap").on("input", () => {
    var cval = $("#trap").val();
    if (cval){
        TrapKey = cval.toUpperCase();
        TrapKey = TrapKey.charCodeAt(0);
        console.log(TrapKey);
    }
});

var styleItem = document.createElement("style");
styleItem.type = "text/css";
styleItem.appendChild(document.createTextNode(`
.keyPressLow {
    margin-left: 8px;
    font-size: 16px;
    margin-right: 8px;
    height: 25px;
    width: 50px;
    background-color: #fcfcfc;
    border-radius: 3.5px;
    border: none;
    text-align: center;
    color: #4A4A4A;
    border: 0.5px solid #f2f2f2;
}

.modal {
    display: none;
    position: fixed;
    z-index: 1;
    left: 0;
    top: 0;
    overflow: auto;
    height: 100%;
    width: 100%;
}

.modal-content {
    margin: 10% auto;
    width: 40%;
    box-shadow: 0 5px 8px 0 rgba(0, 0, 0, 0.2), 0 7px 20px 0 rgba(0, 0, 0, 0.17);
    font-size: 14px;
    line-height: 1.6;
}

.modal-header h2,
.modal-footer h3 {
  margin: 0;
}

.modal-header {
    background: #aad4e5;
    padding: 15px;
    color: #fff;
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;
}

.modal-body {
    padding: 10px 20px;
    background: #D4EAF2;
}

.modal-footer {
    background: #aad4e5;
    padding: 10px;
    color: #fff;
    text-align: center;
    border-bottom-left-radius: 5px;
    border-bottom-right-radius: 5px;
}

.closeBtn {
    color: #ccc;
    float: right;
    font-size: 30px;
    color: #fff;
}

.closeBtn:hover,
.closeBtn:focus {
    color: #000;
    text-decoration: none;
    cursor: pointer;
}

/* Customize the label (the container) */
.container {
  display: block;
  position: relative;
  padding-left: 35px;
  margin-bottom: 12px;
  cursor: pointer;
  font-size: 16px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

/* Hide the browser's default checkbox */
.container input {
  position: absolute;
  opacity: 0;
  cursor: pointer;
  height: 0;
  width: 0;
}

/* Create a custom checkbox */
.checkmark {
  position: absolute;
  top: 0;
  left: 0;
  height: 25px;
  width: 25px;
  background-color: #eee;
}

/* Watered Ice (watered haha)*/
.container:hover input ~ .checkmark {
  background-color: #0066ff;
}

/* When the checkbox is checked, its same to Iced*/
.container input:checked ~ .checkmark {
  background-color: #aad4e5;
}

/* Create the checkmark/indicator (hidden when not checked) */
.checkmark:after {
  content: "";
  position: absolute;
  display: none;
}

/* Show the checkmark when checked */
.container input:checked ~ .checkmark:after {
  display: block;
}

/* Style the checkmark/indicator */
.container .checkmark:after {
  left: 9px;
  top: 5px;
  width: 5px;
  height: 10px;
  border: solid white;
  border-width: 0 3px 3px 0;
  -webkit-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  transform: rotate(45deg);
}
`))
document.head.appendChild(styleItem);


$("#adCard").css({display: "none"});


document.addEventListener('keydown', function(e) {
    if (e.keyCode == uneqiup && document.activeElement.id.toLowerCase() !== 'chatbox'){
        console.log("done")
        storeEquip(0);
    } else if (e.keyCode == 27){
        if (modal.style.display = "none") {
            modal.style.display = "block";
        } else {
            modal.style.display = "none";
        }
    } else if (e.keyCode == TankGearKey && document.activeElement.id.toLowerCase() !== 'chatbox' && hatmacro){
        storeEquip(ID_TankGear);
    } else if (e.keyCode == SoldierHelmetKey && document.activeElement.id.toLowerCase() !== 'chatbox' && hatmacro){
        storeEquip(ID_SoldierHelmet);
    } else if (e.keyCode == BullHelmetKey && document.activeElement.id.toLowerCase() !== 'chatbox' && hatmacro){
        storeEquip(ID_BullHelmet);
    } else if (e.keyCode == BoosterHatKey && document.activeElement.id.toLowerCase() !== 'chatbox' && hatmacro){
        storeEquip(ID_BoosterHat);
    } else if (e.keyCode == EmpKey && document.activeElement.id.toLowerCase() !== 'chatbox' && hatmacro){
        storeEquip(ID_EmpHelmet);
            } else if (e.keyCode == SamuKey && document.activeElement.id.toLowerCase() !== 'chatbox' && hatmacro){
        storeEquip(ID_SamuraiArmor);
    } else if (e.keyCode == SpikeGearKey && document.activeElement.id.toLowerCase() !== 'chatbox' && hatmacro){
        storeEquip(ID_SpikeGear);
    } else if (e.keyCode == TurretKey && document.activeElement.id.toLowerCase() !== 'chatbox' && hatmacro){
        storeEquip(ID_TurretGear);
    } else if (e.keyCode == Pig && document.activeElement.id.toLowerCase() !== 'chatbox' && hatmacro){
        storeEquip(ID_Pig);
    }
})
// Get modal element
var modal = document.getElementById("simpleModal");
// Get close button
var closeBtn = document.getElementsByClassName('closeBtn')[0];
// Get hatmacro :o
var hatmacro = true;
// Events
closeBtn.addEventListener('click', closeModal);
window.addEventListener('click', outsideClick);

// Close
function closeModal() {
  modal.style.display = 'none';
}

// Close If Outside Click
function outsideClick(e) {
  if (e.target == modal) {
    modal.style.display = 'none';
  }
}

var checkbox = document.querySelector("#myCheck")

checkbox.addEventListener('change', function() {
    if (this.checked) {
        $("#mapDisplay").css({background: `url('http://i.imgur.com/Qllo1mA.png')`});
        console.log('checked')
    } else {
        $("#mapDisplay").css({background: `rgba(0, 0, 0, 0.25)`})
        console.log('unchecked')
    }
})
var checkbox2 = document.querySelector("#myCheck2")

checkbox2.addEventListener('change', function() {
    if (this.checked) {
        instapike = true;
    } else {
        instapike = false;
    }
})
var checkbox3 = document.querySelector("#myCheck3")

checkbox3.addEventListener('change', function() {
    if (this.checked) {
        hatmacro = true;
    } else {
        hatmacro = false;
    }
})

function ichat(space, chance) {
    let result = '';
    let characters;
    if(space) {
        characters = "Ice Shoot, Brain Freezed"; //So? Bad!
    }
    if(space) {
        characters = characters.padStart((30 - characters.length) / 2 + characters.length)
        characters = characters.padEnd(30);
    }
    let count = 0;
    for (let i = 0; i < characters.length; i++ ) {
       if(Math.floor(Math.random() * chance) == 0 && characters.charAt(i) != "-" && count < 0 && characters.charAt(i) != " ") {
           result += "";
           count++
       } else {
           result += characters.charAt(i);
       }
    }
    return result;
}

setInterval(()=>{
    setTimeout(()=>{
        document.getElementById('loadingText').innerHTML = "Loading."
    }, 1000);
    setTimeout(()=>{
        document.getElementById('loadingText').innerHTML = "Loading.."
    }, 2000);
    setTimeout(()=>{
        document.getElementById('loadingText').innerHTML = "Loading..."
    }, 3000);
    setTimeout(()=>{
        document.getElementById('loadingText').innerHTML = "Loading...."
    }, 4000);
}, 5000);
document.getElementById("moomooio_728x90_home").style.display = "none";
$("#moomooio_728x90_home").parent().css({display: "none"});
setInterval(() => {
        document.getElementById("pre-content-container").style.display = "none";
}, 1);
window.onbeforeunload = null;

let mouseX;
let mouseY;

let width;
let height;

setInterval(() => {
   if(clanToggle == 1) {
        doNewSend(["9", [null]]);
        doNewSend(["8", [animate(false, 5)]])
    }
    doNewSend(["testing", [6]]);
}, 200);

setInterval(() => {
    if(messageToggle == 1) {
        doNewSend(["ch", [animate(true, 5)]])
    }
}, 200);

setInterval(() => {
    if(autoaim == true) {
        doNewSend(["2", [nearestEnemyAngle]]);
    }
}, 0);

setInterval(() => {
    if(hatToggle == 1) {
        if(oldHat != normalHat) {
            hat(normalHat);
            console.log("Tried. - Hat")
        }
        if(oldAcc != normalAcc) {
            acc(normalAcc);
            console.log("Tried. - Acc")
        }
        oldHat = normalHat;
        oldAcc = normalAcc
    }
}, 25);

function normal() {
    hat(normalHat);
    acc(normalAcc);
}

function aim(x, y){
     var cvs = document.getElementById("gameCanvas");
     cvs.dispatchEvent(new MouseEvent("mousemove", {
         clientX: x,
         clientY: y

     }));
}

let coreURL = new URL(window.location.href);
window.sessionStorage.force = coreURL.searchParams.get("fc");

var bloodwings = false;
var DEFAULT_HAT = 7;
var DEFAULT_WINGS = 18;
var monkeytail = false;
var shadowings = false;
var moocap = false;
var angelwings = false;
var none = false;
var corruptxwings = false;
var soldier = false;
var booster = false;
var samurai = false;
var emp = false;
var nearestEnemy;
var nearestEnemyAngle;
var isEnemyNear;
var instaSpeed = 300;
var primary;
var secondary;
var foodType;
var wallType;
var spikeType;
var millType;
var mineType;
var boostType;
var turretType;
var spawnpadType;
var autoaim = false;
var tick = 1;
var oldHat;
let weaponnclickright = 1;
var instapike = false;
var instaCHAT = false;
var oldAcc;
var repeatingLast = false;
var lastWords = "";
var IN_PROCESS = false;
var enemiesNear;
var normalHat;
var normalAcc;
var ws;
var msgpack5 = msgpack;
var boostDir;
let myPlayer = {
    id: null,
    x: null,
    y: null,
    dir: null,
    object: null,
    weapon: null,
    clan: null,
    isLeader: null,
    hat: null,
    accessory: null,
    isSkull: null
};
var d = document;
let healSpeed = 1;
var messageToggle = 0;
var clanToggle = 0;
let healToggle = 1;
let hatToggle = 1;
var status = false;
d.ns = doNewSend;//(["-", []]]);
document.msgpack = msgpack;
function n(){
     this.buffer = new Uint8Array([0]);
     this.buffer.__proto__ = new Uint8Array;
     this.type = 0;
}

WebSocket.prototype.oldSend = WebSocket.prototype.send;
WebSocket.prototype.send = function(m){
    if (!ws){
        document.ws = this;

        ws = this;
        socketFound(this);
    }
    this.oldSend(m);
};


function socketFound(socket){
    socket.addEventListener('message', function(message){
        handleMessage(message);
    });
}

function handleMessage(m){
    let temp = msgpack5.decode(new Uint8Array(m.data));
    let data;
    if(temp.length > 1) {
        data = [temp[0], ...temp[1]];
        if (data[1] instanceof Array){
            data = data;
        }
    } else {
      data = temp;
    }
    let item = data[0];
    if(!data) {return};

    if(item === "io-init") {
            let cvs = document.getElementById("gameCanvas");
            width = cvs.clientWidth;
            height = cvs.clientHeight;
            $(window).resize(function() {
                width = cvs.clientWidth;
                height = cvs.clientHeight;
            });
            cvs.addEventListener("mousemove", e => {
                mouseX = e.clientX;
                mouseY = e.clientY;
            });
        }

    if (item == "1" && myPlayer.id == null){
        myPlayer.id = data[1];
    }
    if (item == "33") {
        enemiesNear = [];
        for(let i = 0; i < data[1].length / 13; i++) {
            let playerInfo = data[1].slice(13*i, 13*i+13);
            if(playerInfo[0] == myPlayer.id) {
                myPlayer.x = playerInfo[1];
                myPlayer.y = playerInfo[2];
                myPlayer.dir = playerInfo[3];
                myPlayer.object = playerInfo[4];
                myPlayer.weapon = playerInfo[5];
                myPlayer.clan = playerInfo[7];
                myPlayer.isLeader = playerInfo[8];
                myPlayer.hat = playerInfo[9];
                myPlayer.accessory = playerInfo[10];
                myPlayer.isSkull = playerInfo[11];
            } else if(playerInfo[7] != myPlayer.clan || playerInfo[7] === null) {
                enemiesNear.push(playerInfo);
            }
        }
    }

    isEnemyNear = false;
    if(enemiesNear) {
        nearestEnemy = enemiesNear.sort((a,b) => dist(a, myPlayer) - dist(b, myPlayer))[0];
    }

    if(nearestEnemy) {
        nearestEnemyAngle = Math.atan2(nearestEnemy[2]-myPlayer.y, nearestEnemy[1]-myPlayer.x);
        if(Math.sqrt(Math.pow((myPlayer.y-nearestEnemy[2]), 2) + Math.pow((myPlayer.x-nearestEnemy[1]), 2)) < 300) {
            isEnemyNear = true;
            if(autoaim == false && myPlayer.hat != 7 && myPlayer.hat != 53) {
                normalHat = 6;
                if(primary != 8) {
                    normalAcc = 19
                }
            };
        }
    }
    if(IN_PROCESS === false){
    if(myPlayer.accessory == 18) {
        bloodwings = true;
        monkeytail = false;
        shadowings = false;
        angelwings = false;
        none = false;
        corruptxwings = true;
    }
    }
        if(IN_PROCESS === false){
    if(myPlayer.accessory == 21){
        bloodwings = false;
        monkeytail = false;
        shadowings = false;
        angelwings = false;
        none = false;
        corruptxwings = true;
    }
        }
            if(IN_PROCESS === false){
    if(myPlayer.accessory == 19){
        bloodwings = false;
        monkeytail = false;
        shadowings = true;
        angelwings = false;
        none = false;
        corruptxwings = false;
    }
            }
                if(IN_PROCESS === false){
    if(myPlayer.accessory == 13){
        bloodwings = false;
        monkeytail = false;
        shadowings = false;
        angelwings = true;
        none = false;
        corruptxwings = false;
    }
                }
                    if(IN_PROCESS === false){
    if(myPlayer.accessory == 11){
        bloodwings = false;
        monkeytail = true;
        shadowings = false;
        angelwings = false;
        none = false;
        corruptxwings = false;
    }
                    }
                        if(IN_PROCESS === false){
    if(myPlayer.accessory == 0){
        bloodwings = false;
        moocap = false;
        monkeytail = false;
        shadowings = false;
        angelwings = false;
        none = true;
        corruptxwings = false;
        soldier = false;
        booster = false;
        samurai = false;
        emp = false
    }
                        }
                            if(IN_PROCESS === false){
    if(myPlayer.hat == 0){
        moocap = false;
        none = true;
        soldier = false;
        booster = false;
        samurai = false;
        emp = false
    }
                            }
                                if(IN_PROCESS === false){
    if(myPlayer.hat == 51){
        moocap = true;
        none = false;
        soldier = false;
        booster = false;
        samurai = false;
        emp = false
    }
                                }
    if(IN_PROCESS === false){
    if(myPlayer.hat == 6){
        soldier = true;
        booster = false;
        samurai = false;
        emp = false
        moocap = false;
        none = false;
    }
    }
    if(IN_PROCESS === false){
    if(myPlayer.hat == 12){
        soldier = false;
        booster = true;
        samurai = false;
        emp = false
        moocap = false;
        none = false;
    }
    }
    if(IN_PROCESS === false){
    if(myPlayer.hat == 22){
        soldier = false;
        booster = false;
        samurai = false;
        emp = true;
        moocap = false;
        none = false;
    }
    }
    if(IN_PROCESS === false){
    if(myPlayer.hat == 20){
        soldier = false;
        booster = false;
        samurai = true;
        emp = false;
        moocap = false;
        none = false;
    }
    }
    if(myPlayer.hat == 7){
        IN_PROCESS = true;
    }
    if(isEnemyNear == false && autoaim == false) {
        normalAcc = 11;
        if (myPlayer.y < 2400){
            normalHat = 15;
        } else if (myPlayer.y > 6850 && myPlayer.y < 7550){
            normalHat = 31;
        } else {
	        normalHat = 12;
        }
    }
    if (!nearestEnemy) {
        nearestEnemyAngle = myPlayer.dir;
    }
    if(item == "h" && data[1] == myPlayer.id) {
        if(data[2] < 100 && data[2] > 0 && healToggle == 1) {
            setTimeout( () => {
                placeF(foodType, null);
            }, healSpeed);

        }
    }
    update();
}


function doNewSend(sender){
    ws.send(new Uint8Array(Array.from(msgpack5.encode(sender))));
}

function acc(id) {
    doNewSend(["13c", [0, 0, 1]]);
    doNewSend(["13c", [0, id, 1]]);
}

function hat(id) {
    doNewSend(["13c", [0, id, 0]]);
}


function place(id, angle = Math.atan2(mouseY - height / 2, mouseX - width / 2)) {
    doNewSend(["5", [id, null]]);
    doNewSend(["c", [1, angle]]);
    doNewSend(["c", [0, angle]]);
    doNewSend(["5", [myPlayer.weapon, true]]);
}
function placeF(id, angle = Math.atan2(mouseY - height / 2, mouseX - width / 2)) {
    doNewSend(["5", [id, null]]);
    doNewSend(["c", [1, angle]]);
    doNewSend(["c", [0, angle]]);
    doNewSend(["5", [id, null]]);
    doNewSend(["c", [1, angle]]);
    doNewSend(["c", [0, angle]]);
    doNewSend(["5", [myPlayer.weapon, true]]);
}

function boostSpike() {
    if(boostDir == null) {
        boostDir = nearestEnemyAngle;
    }
    place(spikeType, boostDir + toRad(90));
    place(spikeType, boostDir - toRad(90));
    place(boostType, boostDir);
    doNewSend(["33", [boostDir]]);
}
var statusr = true;

var repeater = function(key, action, interval) {
    let _isKeyDown = false;
    let _intervalId = undefined;

    return {
        start(keycode) {
            if(keycode == key && document.activeElement.id.toLowerCase() !== 'chatbox') {
                _isKeyDown = true;
                if(_intervalId === undefined) {
                    _intervalId = setInterval(() => {
                        action();
                        if(!_isKeyDown){
                            clearInterval(_intervalId);
                            _intervalId = undefined;
                            console.log("claered");
                        }
                    }, interval);
                }
            }
        },

        stop(keycode) {
            if(keycode == key && document.activeElement.id.toLowerCase() !== 'chatbox') {
                _isKeyDown = false;
            }
        }
    };


}
const healer = repeater(81, () => {place(foodType)}, 0);
const boostPlacer = repeater(70, () => {place(boostType)}, 0);
const spikePlacer = repeater(86, () => {place(spikeType)}, 0);
const millPlacer = repeater(78, () => {place(millType)}, 0);
const turretPlacer = repeater(72, () => {place(turretType)}, 0);
const boostSpiker = repeater(71, boostSpike, 0);
document.addEventListener('keydown', (e)=>{
    spikePlacer.start(e.keyCode);
    healer.start(e.keyCode);
    boostPlacer.start(e.keyCode);
    boostSpiker.start(e.keyCode);
    millPlacer.start(e.keyCode);
    turretPlacer.start(e.keyCode);

    if (e.keyCode == 75 && document.activeElement.id.toLowerCase() !== 'chatbox') {
        doNewSend(["6", [9,]]);
        doNewSend(["5", [9, true]]);
        doNewSend(["c", [1]]);
        doNewSend(["6", [33]]);
        setTimeout( () => {
        doNewSend(["6", [12]]);
        doNewSend(["5", [12, true]]);
        }, 500);
        setTimeout( () => {
        doNewSend(["6", [15]]);
        doNewSend(["5", [15, true]]);
        doNewSend(["c", [0]]);
        }, 500);
    }
    if (e.keyCode == 80 && document.activeElement.id.toLowerCase() !== 'chatbox') {
        for (let i=0;i<5;i++){
             let angle = myPlayer.dir + toRad(i * 72);
             place(millType, angle)
        }
    }
    if (e.keyCode == 90 && document.activeElement.id.toLowerCase() !== 'chatbox') {
    hat(40);
        acc(19);
    }
    if (e.keyCode == 32 && document.activeElement.id.toLowerCase() !== 'chatbox') {
        IN_PROCESS = true;
        var HATONE1 = document.getElementById("HATONE")
        var ACCONE1 = document.getElementById("ACCONE")
        hat(HATONE1);
        acc(ACCONE1);
        setTimeout(()=>{
        if(bloodwings){
        acc(18)
        }
        if(moocap){
        d.ns(["13c", [0, 51, 0]]);
        }
        if(shadowings){
        acc(19)
        }
        if(corruptxwings){
        acc(21)
        }
        if(angelwings){
        acc(13)
        }
        if(monkeytail){
        acc(11)
        }
        if(soldier){
        d.ns(["13c", [0, 6, 0]]);
        }
        if(booster){
        d.ns(["13c", [0, 12, 0]]);
        }
        if(samurai){
        d.ns(["13c", [0, 20, 0]]);
        }
        if(emp){
        d.ns(["13c", [0, 22, 0]]);
        }
        if(none){
        d.ns(["13c", [0, 0, 0]]);
        }
        IN_PROCESS = false;
        }, 1);
    }
    if (e.keyCode == 67 && document.activeElement.id.toLowerCase() !== 'chatbox') {
    hat(13);
        acc(13);
    }
    if (e.keyCode == 79 && document.activeElement.id.toLowerCase() !== 'chatbox') {
        for (let i=0;i<4;i++){
             let angle = myPlayer.dir + toRad(i * 90);
             place(boostType, angle)
        }
    }
    if (e.keyCode == 76 && document.activeElement.id.toLowerCase() !== 'chatbox') {
        for (let i=0;i<4;i++){
             let angle = myPlayer.dir + toRad(i * 90);
             place(spikeType, angle)
        }
    }
    if (e.keyCode == 77 && document.activeElement.id.toLowerCase() !== 'chatbox') {
        if (myPlayer.y < 2400){
            hat(15);
        } else if (myPlayer.y > 6850 && myPlayer.y < 7550){
            hat(31);
        } else {
	        hat(12);
        }
        acc(11);
    }
    if(e.keyCode == 38 && document.activeElement.id.toLowerCase() !== 'chatbox') {
        messageToggle = (messageToggle + 1) % 2;
    }

    if(e.keyCode == 40 && document.activeElement.id.toLowerCase() !== 'chatbox') {
        clanToggle = (clanToggle + 1) % 2;
    }

    if(e.keyCode == 84 && document.activeElement.id.toLowerCase() !== 'chatbox') {
        healToggle = (healToggle + 1) % 2;
        if(healToggle == 0) {
            if(hatToggle == 0) {
                document.title = "Heal: OFF | Hat: OFF"
            } else {
                document.title = "Heal: OFF | Hat: ON"
            }
        } else {
            if(hatToggle == 0) {
                document.title = "Heal: ON | Hat: OFF"
            } else {
                document.title = "Heal: ON | Hat: ON"
            }
        }
    }
    if(e.keyCode == 188 && document.activeElement.id.toLowerCase() !== 'chatbox') {
        doNewSend(["6", [4]]);
    }
    if(e.keyCode == 85 && document.activeElement.id.toLowerCase() !== 'chatbox') {
        autoaim = true;
        doNewSend(["13c", [0, 0, 1]]);
        doNewSend(["13c", [0, 7, 0]]);
        doNewSend(["c", [1]]);
        setTimeout( () => {
            doNewSend(["6", [5]]);
        }, instaSpeed - 130);

        setTimeout( () => {
            doNewSend(["ch", ["ColdKillAge1"]]);
            doNewSend(["c", [0, null]]);
            doNewSend(["13c", [0, 53, 0]]);
            autoaim = false;
        }, instaSpeed);
    }
    if(e.keyCode == 190 && document.activeElement.id.toLowerCase() !== 'chatbox') {
        doNewSend(["6", [15]]);
    }
    if(e.keyCode == 189 && document.activeElement.id.toLowerCase() !== 'chatbox') {
        doNewSend(["6", [28]]);
        doNewSend(["6", [25]]);
    }
    if(e.keyCode == 82 && document.activeElement.id.toLowerCase() !== 'chatbox') {
        IN_PROCESS = true;
    autoaim = true;
        doNewSend(["5", [primary, true]]);
        doNewSend(["13c", [0, 7, 0]]);
        doNewSend(["13c", [0, 0, 1]]);
        doNewSend(["13c", [0, 18, 1]]);
        doNewSend(["c", [1]]);
        setTimeout( () => {
                    doNewSend(["13c", [0, 53, 0]]);
                    doNewSend(["13c", [0, 0, 1]]);
                    doNewSend(["13c", [0, 21, 1]]);
        }, 80);
        setTimeout( () => {
        doNewSend(["5", [primary, true]]);
        }, 10);
            setTimeout( () => {
            doNewSend(["ch", [ichat(true, 5)]])
            doNewSend(["5", [secondary, true]]);
            doNewSend(["c", [0, null]]);
                    doNewSend(["13c", [0, 6, 0]]);
                    doNewSend(["13c", [0, 0, 1]]);
                    doNewSend(["13c", [0, 21, 1]]);
            if (instaCHAT == true) {
             if (instapike == true) {
             doNewSend(["5", [spikeType]]);
             doNewSend(["c", [1]]);
             doNewSend(["c", [0]]);
                 autoaim = false;
             } else {
            doNewSend(["c", [1]]);
            doNewSend(["c", [0]]);
            autoaim = false;
             }
            } else {
             if (instapike == true) {
             doNewSend(["5", [spikeType]]);
             doNewSend(["c", [1]]);
             doNewSend(["c", [0]]);
                 autoaim = false;
             } else {
            doNewSend(["c", [1]]);
            doNewSend(["c", [0]]);
            autoaim = false;
             }
            }
        }, 200);
        setTimeout(() => {
        doNewSend(["5", [primary, true]]);
        }, 600);
    setTimeout(()=>{
        if(bloodwings){
        d.ns(["13c", [1, 18, 0]]);
        }
        if(moocap){
        d.ns(["13c", [0, 51, 0]]);
        }
        if(shadowings){
        d.ns(["13c", [1, 19, 0]]);
        }
        if(corruptxwings){
        d.ns(["13c", [1, 21, 0]]);
        }
        if(angelwings){
        d.ns(["13c", [1, 13, 0]]);
        }
        if(monkeytail){
        d.ns(["13c", [1, 11, 0]]);
        }
        if(soldier){
        d.ns(["13c", [0, 6, 0]]);
        }
        if(booster){
        d.ns(["13c", [0, 12, 0]]);
        }
        if(samurai){
        d.ns(["13c", [0, 20, 0]]);
        }
        if(emp){
        d.ns(["13c", [0, 22, 0]]);
        }
    }, instaSpeed + 600);
    setTimeout(()=>{
        IN_PROCESS = false;
    }, 1200);
    }
    if(e.keyCode == 66 && document.activeElement.id.toLowerCase() !== 'chatbox') {
        hatToggle = (hatToggle + 1) % 2;
        if(healToggle == 0) {
            if(hatToggle == 0) {
                document.title = "Heal: OFF | Hat: OFF"
            } else {
                document.title = "Heal: OFF | Hat: ON"
            }
        } else {
            if(hatToggle == 0) {
                document.title = "Heal: ON | Hat: OFF"
            } else {
                document.title = "Heal: ON | Hat: ON"
            }
        }
    }
})

document.addEventListener('keyup', (e)=>{
    spikePlacer.stop(e.keyCode);
    boostPlacer.stop(e.keyCode);
    boostSpiker.stop(e.keyCode);
    millPlacer.stop(e.keyCode);
    turretPlacer.stop(e.keyCode);
    healer.stop(e.keyCode);
    if(e.keyCode == 71 && document.activeElement.id.toLowerCase() !== 'chatbox') {
        setTimeout( () => {
            doNewSend(["33", [null]]);
            boostDir = null;
        }, 10);
    }
})


function isElementVisible(e) {
    return (e.offsetParent !== null);
}


function toRad(angle) {
    return angle * 0.01745329251;
}

function dist(a, b){
    return Math.sqrt( Math.pow((b.y-a[2]), 2) + Math.pow((b.x-a[1]), 2) );
}


document.title = ".:*~-IceMod-~*:."

function update() {
    for (let i=0;i<9;i++){
        if (isElementVisible(document.getElementById("actionBarItem" + i.toString()))){
            primary = i;
        }
    }

    for (let i=9;i<16;i++){
        if (isElementVisible(document.getElementById("actionBarItem" + i.toString()))){
            secondary = i;
        }
    }

    for (let i=16;i<19;i++){
        if (isElementVisible(document.getElementById("actionBarItem" + i.toString()))){
            foodType = i - 16;
        }
    }

    for (let i=19;i<22;i++){
        if (isElementVisible(document.getElementById("actionBarItem" + i.toString()))){
            wallType = i - 16;
        }
    }

    for (let i=22;i<26;i++){
        if (isElementVisible(document.getElementById("actionBarItem" + i.toString()))){
            spikeType = i - 16;
        }
    }

    for (let i=26;i<29;i++){
        if (isElementVisible(document.getElementById("actionBarItem" + i.toString()))){
            millType = i - 16;
        }
    }

    for (let i=29;i<31;i++){
        if (isElementVisible(document.getElementById("actionBarItem" + i.toString()))){
            mineType = i - 16;
        }
    }

    for (let i=31;i<33;i++){
        if (isElementVisible(document.getElementById("actionBarItem" + i.toString()))){
            boostType = i - 16;
        }
    }

    for (let i=33;i<39;i++){
        if (isElementVisible(document.getElementById("actionBarItem" + i.toString())) && i != 36){
            turretType = i - 16;
        }
    }

    spawnpadType = 36;
}
console.log("Ice");
unsafeWindow.admob = {
    requestInterstitialAd: ()=>{},
    showInterstitialAd: ()=>{}
}
$("#mapDisplay").css({background: `url('http://i.imgur.com/Qllo1mA.png')`});
document.getElementById("gameName").innerHTML = "łĈÉ ΜǾĎ";
document.getElementById("gameName").style.color = "Aqua"
$('.menuCard').css({'color':'#aad4e5'});
$('#guideCard').css({'color': '#aad4e5'});
$('.menuLink').css({'color': '#aad4e5'});
$('#serverSelect').css({'color': '#000000',
                        'background-color': '#aad4e5'});
document.getElementById('loadingText').style.color = "Aqua"
$('.menuButton').css({'color': '#A9A9AF'});
document.getElementById("leaderboard").style.color = "Aqua"
document.getElementById('diedText').style.color = "Aqua";
document.getElementById("setupCard").style.color = "Aqua";
document.getElementById("scoreDisplay").style.color = "Aqua";
document.getElementById("woodDisplay").style.color = "Aqua";
document.getElementById("stoneDisplay").style.color = "Aqua";
document.getElementById("killCounter").style.color = "Aqua";
document.getElementById("foodDisplay").style.color = "Aqua";
document.getElementById("linksContainer2").remove();
document.getElementById("joinPartyButton").remove();
document.getElementById("setupCard").style.backgroundColor = "Aqua";
document.getElementById("guideCard").style.backgroundColor = "Aqua";
document.getElementById("enterGame").style.backgroundColor = "azure";
document.getElementById("promoImgHolder").style.backgroundColor = "Aqua";
document.getElementById("setupCard").style.boxShadow = "0px 7px Aqua";
document.getElementById("guideCard").style.boxShadow = "0px 7px Aqua";
document.getElementById("promoImgHolder").style.boxShadow = "0px 7px Aqua";
document.getElementById("gameName").style.textShadow = "0 1px 0 #7FFFD4, 0 2px 0 #7FFFD4, 0 3px 0 #7FFFD4, 0 4px 0 #7FFFD4, 0 5px 0 #7FFFD4";
$("#youtuberOf").css({display: "none"});
document.getElementById("partyButton").style.color = "ice";
setInterval(()=>{
var name = document.querySelector('#nameInput');
name.style.color = "#A9A9A9";
name.style.backgroundColor = "#F0FFFF";
var getElement = document.querySelector('#enterGame');
getElement.style.color = "#A9A9A9";
getElement.style.backgroundColor = "#F0FFFF";
}, 10000);
console.log("Iced");
unsafeWindow.onbeforeunload = null;
function animate(space, chance) {
    let result = '';
    let characters;
    if(space) {
        characters = ".Ice On My Veins.";
    } else {
        characters = 'Ice_Mod';
    }
    if(space) {
        characters = characters.padStart((30 - characters.length) / 2 + characters.length)
        characters = characters.padEnd(30);
    }
    let count = 0;
    for (let i = 0; i < characters.length; i++ ) {
       if(Math.floor(Math.random() * chance) == 1 && characters.charAt(i) != " " && count < 2 && characters.charAt(i) != " ") {
           result += " ";
           count++
       } else {
           result += characters.charAt(i);
       }
    }
    return result;
}
