# Realtime Bitcoin Price Tracker

This is a simple dashboard for tracking realtime pricing updates on Bitcoin powered by the powerful PubNub network.

![Screenshot of Demo](screenshot1.jpg)

Currently, the application only updates every 10 seconds, however this is very easy to change.  In the setInterval javascript function, you can change the 10,000 milliseconds number to whatever you wish:

```
setInterval(function(){
    xhr.open('GET', 'https://min-api.cryptocompare.com/data/pricemulti?fsyms=BTC&tsyms=USD', true)
    xhr.send();
    xhr.onreadystatechange = processRequest;
}, 10000)
```

Make sure to replace the Publish Subscribe keys with your own keys in your PubNub Admin Dashboard.