# Reverse string method

### Step-1
##### In-built functions

```javascript
var test = "SURESH";
test.split("").reverse().join("");

Output 
======
"HSERUS"
```

### Step-2
##### Decrementing for-loop with concatenation

```javascript
function reverse(s) {
  var o = '';
  for (var i = s.length - 1; i >= 0; i--)
    o += s[i];
  return o;
}

reverse('SURESH');

Output 
======
"HSERUS"
```

### Step-3 
##### Incrementing/decrementing for-loop with two arrays

```javascript
function reverse(s) {
  var o = [];
  for (var i = s.length - 1, j = 0; i >= 0; i--, j++) {
    o[j] = s[i];
  }
  return o.join('');
}

reverse('SURESH');

Output 
======
"HSERUS"
```

### Step-4 
##### Incrementing for-loop with array pushing and charAt

```javascript
function reverse(s) {
  var o = [];
  for (var i = 0, len = s.length; i <= len; i++) {
    o.push(s.charAt(len - i));
  }
  return o.join('');
}

reverse('SURESH');

Output 
======
"HSERUS"
```


### Step-5 
##### Recursion with substring and charAt

```javascript
function reverse(s) {
  return (s === '') ? '' : reverse(s.substr(1)) + s.charAt(0);
}

reverse('SURESH');

Output 
======
"HSERUS"
```
