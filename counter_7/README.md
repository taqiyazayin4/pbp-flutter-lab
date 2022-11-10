# Tugas 7 PBP 
## Nama : Taqiya Zayin Hanafie 
## NPM : 2106751335

#### Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget dan jelaskan perbedaan dari keduanya.
Stateless widget adalah ketika suatu widget tidak akan melakukan perubahan sdan hanya memiliki final property sehingga memiliki sifat statis dan immutable. Stateless widget akan mem-override build() dan return Widget. Contoh: Icon, Text

Stateful widget adalah suatu widget yang akan melakukan perubahan secara dinamis ketika user melakukan interaksi dengan widget tersebut. Stateful widget akan mem-override CreateState() dan return State. Pada saat state suatu widget berubah, object state memanggil setState dan menotifikasi framework untuk redraw widget. Contoh: Textfield, Checkbox, Radio button


<br />

#### Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya.
Pada tugas 7 ini, saya memanfaatkan widget Text yang berfungsi untuk menampilkan sebuah text/string. Selain itu, terdapat FloatingActionButton yang memiliki fungsi untuk
menjalankan suatu fungsi pada saat button tersebut ditekan.

<br />

#### Apa fungsi dari setState()? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.
setState() memiliki fungsi untuk merebuild widget dan turunannya. setState() akan menotifikasi State Object dan mengupdate UI widget tersebut. Variabelyang terdampak oleh fungsi setState() yaitu _counter dan keterangan.
<br />

#### Jelaskan perbedaan antara const dengan final.
final diinisiasi pada saat runtime dan diassingn satu kali. Dapat didefiniskan pada class maupun method. final akan terinisiasi ulang pada saat state ter-update

const diinisiasi pada saat compile time. Dapat didefinisikan pada method. const akan terinisiasi ulang pada saat state terupdate.

<br />

#### Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas.

1. Membuat sebuah program Flutter baru dengan nama counter_7 dengan menjalankan perintah flutter create counter_7
2. Mengubah tampilan dengan menambahkan title: 'Program Counter' pada home dan melakukan pembuatan FloatingActionButton dan text sesuai dengan tampilan pada soal.
3. Mengimplementasikan logika tombol + dan - serta menampilkan teks indikator sesuai dengan counter.
 <br /> 
 
method untuk increment dan decrement
 ``` shell

  void _incrementCounter() {
    setState(() {
      
      _counter++;
      if(_counter%2==0){
        keterangan = "Genap";
      }
      else{
        keterangan = "Ganjil";
      }
    });
  }

  void _decrementCounter() {
    setState(() {
      
      if(_counter!=0){
        _counter--;
      }
      if(_counter%2==0){
        keterangan = "Genap";
      }
      else{
        keterangan = "Ganjil";
      }
      
    });
  }


```
teks indikator dan counter
``` shell

children: <Widget>[
            
            Text(
              keterangan,
              style: TextStyle(color:getColor()),
            ),
            Text(
              '$_counter',
              style: Theme.of(context).textTheme.headline4,
            ),
          ],
        ),
      ),
```

 <br /> 