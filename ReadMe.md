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

#### Options
