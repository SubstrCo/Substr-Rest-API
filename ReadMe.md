# Substr API

## Service Fee

### GET `https://www.substr.co/api/fee/{location}`

#### Options

- jaro
- molo
- baluarte
- calumpang
- lapaz
- cityProper
- mandurriao
- tagbac
- oton
- villa
- pavia
- ungka
- staBarbara

##### Example using fetch

`ES6 & up`

```javascript
const response = await fetch('https://www.substr.co/api/fee/jaro');
const serviceFee = await response.json();
console.log(serviceFee); // output => { serviceFee: 90 }
```

`Traditional`

```javascript
fetch('http://www.substr.co/api/fee/jaro').then(function(response) {
  response.json().then(function(serviceFee) {
    console.log(serviceFee); // output => { serviceFee: 90 }
  });
});
```

## Create Request

### POST `https://www.substr.co/api/request`

#### Api-key

#### AIzaSyA8pe8s2-tPaJpraIF6knVZnRLqLK1RCAw

##### Example using post

`ES6 & up`

```javascript
const createRequest  = await fetch('https://www.substr.co/api/request', 
    {
      headers: {
        authorization: 'Bearer AIzaSyA8pe8s2-tPaJpraIF6knVZnRLqLK1RCAw' 
      },
      method: 'POST',
      body: JSON.stringify(
        {
          clientName: 'Mike Tyson', 
          contactNumber: '09997796417', 
          items: [ 
            {itemName: 'Milo', quantity: 3}, 
            {itemName: 'Bear Brand', quantity: 10}, 
            {itemName: 'MikMik', quantity: 2} 
          ],
          deliveryAddress: 'San Isidro, Jaro, Ilo-ilo City', 
          branchAddress: 'IS Atrium', 
          amount: 1500, 
          note:'Juan Carlos Store' 
        }
      ),
    }
  );
const result = await createRequest.json();
console.log(result) // {success: true}
```

`Traditional`

```javascript
fetch('https://www.substr.co/api/request', 
    {
      headers: {
        authorization: 'Bearer AIzaSyA8pe8s2-tPaJpraIF6knVZnRLqLK1RCAw' 
      },
      method: 'POST',
      body: JSON.stringify(
        {
          clientName: 'Mike Tyson', 
          contactNumber: '09997796417', 
          items: [ 
            {itemName: 'Milo', quantity: 3}, 
            {itemName: 'Bear Brand', quantity: 10}, 
            {itemName: 'MikMik', quantity: 2} 
          ],
          deliveryAddress: 'San Isidro, Jaro, Ilo-ilo City', 
          branchAddress: 'IS Atrium', 
          amount: 1500, 
          note:'Juan Carlos Store' 
        }
      ),
    }
  ).then(function(response) {
  response.json().then(function(myJson) {
    console.log(myJson); // output => {"success":true}
  });
});
```
