# dynamic table row using javascript     

We create a table and a form with 2 input field for name and email. User will give value to name and email field. when user submit button we will get the value from name field and email field and insert those name and email value to table by dynamic table.          

I documented those dynamic table as comment   

~~~js
var button = document.getElementById('button');

button.addEventListener('click', function () {
  // extract name from input field
  var name = document.getElementById('name').value;
  // create a text node for name
  var nameNode = document.createTextNode(name);
  // extract email form input field
  var email = document.getElementById('email').value;
  // create a text node for email
  var emailNode = document.createTextNode(email);
  //create a td for name tdname
  var tdName = document.createElement('td');
  //append nameNode to tdname
  tdName.appendChild(nameNode);
  //create a td for email tdemail
  var tdEmail = document.createElement('td');
  //append emailNode tdemail
  tdEmail.appendChild(emailNode);
  //create a tr element
  var tr = document.createElement('tr');
  // append tdname and tdemail to tr
  tr.appendChild(tdName);
  tr.appendChild(tdEmail);
  // select table and append tr to table
  var table = document.getElementById('table');
  table.appendChild(tr);
  document.getElementById('name').value = '';
  document.getElementById('email').value = '';
});
~~~


We first select button. Then added click event listener using `addEventListener` method.     

