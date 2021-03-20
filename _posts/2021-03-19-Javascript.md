---
published: true
---
Javascript adalah high level language, scripting, untyped, and interpreted.

Client side:
- Native Javascript
- JQuery

Server side
- NodeJS
- ExpressJS

## Tipe Data
- number
  - interger
  - 
  
- string
  - ""
  - ''
  - \u
  
- boolean
- object
- function
- undefined


## variable
- var
var namaVariable;

- let

- const

## popup box
- alert()
- prompt()
- confirm()

## Control Flow
- **pengulangan**
  - **for**
    ```
    for(nilaiAwal;kondisi;increment/decrement){
    	aksi;
    }
    ```
  - **do**
  - **while**
    ```
    while(kondisi){
    	aksi;
    }
    ```
- **percabangan**
  - **if**
    ```
    if(kondisi){
    	aksi;
    }
    ```
  - **if else**
  - **if else if**
  - **switch**
    ```
    switch(ekspresi){
    case "nilai 1":
		aksi;
        break;
    default:
		aksi;
        break;
    }
    ```
    
## Function
- **function declaration**
  ```
  function jumlah(a,b){
  	var total = a+b;
    return total;
  }
  ```
  
- **function expression**
  ```
  var jumlahDuaBilangan = function(a,b){
  	var total = a+b;
    return total;
  }
  ```
  
- **arguments**

  array argumen
  
- **refactoring**

  penyerderhanaan agar hemat memori

- **scope**
  - function scope
  
    pake sistem var local function dan global
    
## Array
```
var x = [1,2,3];
```

- method untuk array
  - length
  - join
  - push, pop, unshift, shift
  - slice
  - splice
    ```
    x.slice(indexAwal, berapaHapus, tambah);
    ```
  - sort
  
    jika dua digit:
    
    ```
    angka.sort(function(a,b){
    	return a-b;
    });
    ```
    
  - filter and find
  
    find 1, filter banyak
    
    ```
    var angka2 = angka.find(function(x){
    	return x > 5;
    });
    
    var angka2 = angka.filter(function(x){
    	return x > 5;
    });
    ```
    
## Foreach and Map
```
angka.forEach(function(e, i){
	console.log(e);
});


var angka2 = angka.map(function(e){
	return e*2;
});
```

