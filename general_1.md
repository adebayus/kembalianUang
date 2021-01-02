### Aplikasi Yang Digunakan

1. Vs Code

### Cara Menjalakan Aplikasi

2. node "nama_file.js"

### Sedikit Penjelasan

1. mendeklarasikan array berisi uang pecahan
```javascript
const pecahan = [100000, 50000, 20000, 10000, 5000, 2000, 1000, 500, 200 , 100];
```

2. membuat function untuk menghitung kembalian
```javascript
function hitungUangKembalian(uangBayar, totalBayar) {
	console.log("Uang Dibayarkan : ", uangBayar);
	console.log("Total Bayar : ", totalBayar);
	console.log(`\n`, "===================");

	var totalKembalian = uangBayar - totalBayar;
    
    // console.log(totalKembalian);
    var tempFor = totalKembalian;
    for (let index = 0; index < pecahan.length; index++) {
        tempFor
        if (tempFor>=pecahan[index]){
            var jenis = "lembar"
            if(pecahan[index] < 1000 ){
                jenis = "buah"
            }
            var banyakPecahan = Math.floor(tempFor / pecahan[index])
            tempFor = tempFor - (pecahan[index] * banyakPecahan)
            console.log(`Uang Pecahan RP ${pecahan[index]} sebanyak ${banyakPecahan} ${jenis}` )
        }
    }

    console.log(`\n`, "===================");
    var kembalianLocale = totalKembalian.toLocaleString(['ban', 'id'])
    console.log(`kembalian : Rp ${kembalianLocale}`)
    

}
```

3. memanggil fungsi yang sudah dibuat

```javascript
hitungUangKembalian(200000, 184600);
```