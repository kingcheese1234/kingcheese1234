// Create a button element.
var button = document.createElement("button");
// Set the button's text.
button.innerHTML = "Turn TV Off";
// Add an event listener to the button.
button.addEventListener("click", function() {
  // Get the TV's IP address.
  var ipAddress = "192.168.1.1";
  // Send a command to the TV to turn it off.
  var command = "poweroff";
  // Create a new XMLHttpRequest object.
  var xhr = new XMLHttpRequest();
  // Open a connection to the TV.
  xhr.open("GET", "http://" + ipAddress + "/command/" + command);
  // Send the request.
  xhr.send();
});
// Add the button to the document.
document.body.appendChild(button);
