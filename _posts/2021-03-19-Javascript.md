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

## object
```
var orang = {
	nama : "ryan",
    umur : 20;
}
```

- properti => variable dalam object
- method => fungsi dalam object
- Buat object
```
function Mahasiswa(nama, nrp){
	this.nama = nama;
    this.nrp = nrp;
}

var mhs1 = new Mahasiswa("ryan", "12323");
```

## Advanced Javascript

### object
1. object literal

```
let mahasiswa = {
	nama: "ryan",
    energi: 10,
    makan: function(porsi){
    	this.energi += porsi;
        console.log(`Halo ${this.nama}, selamat makan!`);
	}
}
```

2. function decleration

```
function Mahasiswa(nama,energi){
	let mahasiswa = {}
    mahasiswa.nama = nama;
    mahasiswa.energi = energi;
    
    mahasiswa.makan = function(porsi){
    	this.energi += porsi;
        console.log(`Halo ${this.nama}, selamat makan!`)
    }
    return mahasiswa;
}
```

3. constructor

```
function Mahasiswa(nama,energi){
    this.nama = nama;
    this.energi = energi;
    
    this.makan = function(porsi){
    	this.energi += porsi;
        console.log(`Halo ${this.nama}, selamat makan!`)
    }
}
```

### Object.create()
```
const methodMahasiswa = {
 	makan: function(porsi){
    	this.energi += porsi;
        console.log(console.log(`Halo ${this.nama}, selamat makan!`)
}

function Mahasiswa(nama,energi){
	let mahasiswa = Object.create(methodMahasiswa)
    mahasiswa.nama = nama;
    mahasiswa.energi = energi;  
    }
    return mahasiswa;
}
```

### Prototype
```
function Mahasiswa(nama,energi){
    this.nama = nama;
    this.energi = energi;
}

Mahasiswa.prototype.makan = function(porsi){
	this.energi += porsi;
    return `Halo ${this.nama}, selamat makan!`;
}
```

class

```
class Mahasiswa {
	constructor(nama,energi){
		this.nama = nama;
        this.energi = energi;
    }
    makan(porsi){
    	this.energi += porsi;
    	return `Halo ${this.nama}, selamat makan!`;
    }
}
```

### Closures
- Kombinasi antara function yang memiliki access ke parent scope.

```
function init(){
	let nama = "ryan";
    function tanmpilNama(){  //closure
     console.log(nama);
    }
    tampilNama();
}


function ucapkanSalam(waktu){
	retrun function (nama){
		console.log("terserah");
    }
}

let selamatPagi = ucapkanSalam("Pagi");
selamatPagi("Ryan");
```

- Execution context, hoisting, scope
- alasan menggunakan closure
  - membuat function factory


### Arrow function
Function expression lebih ringkas

```
let tampilPesan = (nama) => {
	return `Halo, ${nama}`;
}
```
- tak cocok untuk constructor kecuali untuk methodnya