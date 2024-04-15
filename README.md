# nolo8
const express = require('express');
const app = express(); const port = 3000;
app.use(express.urlencoded({ extended: true }));
// for parsing application/x-www-form-urlencoded app.get('/', (req, res)
=> { res.sendFile(__dirname + '/index.html');
// send HTML file on GET request });
app.post('/submit-form', (req, res) => { const username =
req.body.username; // access form data // Add validation logic here
res.send(`Username is $aakinbol`);
}); app.listen(port, () => { console.log(`Server running on
http://localhost:${port}`); });
<!DOCTYPE html> <html> <head> <title>Simple Form</title> </head> <body>
<form action="/submit-form" method="post"> <label
for="username">Username:</label> <input type="text" id="username"
name="username" required> <button type="submit">Submit</button> </form>
</body> </html>
post('/submit-form' , (req, res) => {
const Submitted = req.body.Submitted; // access form data

res.send('Form Submitted');
