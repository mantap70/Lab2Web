# Praktikum CSS Dasar

```
Nama    : Fathan Atallah Rasya Nugraha
NIM     : 312410425
Kelas   : TI.24.A3
```

## STRUKTUR REPOSITORY
```
Lab2Web/
│── main.html
│── style.css
│── README.md
```

## Pertanyaan Dan Tugas
### 1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.
#### Jawaban
```css
.button {
    padding: 15px 20px;
    background: #bebcbd;
    color: #fff;
    display: inline-block;
    margin: 10px;
    text-decoration: none;
    transition: 0.7s;
}
.btn-primary {
    background: #E42A42;
}
.button:hover {
    transition: 0.7s;
    color: #E42A42;
    background: #4c2ae4;
    padding: 20px 25px;
}
```
Saya Melakukan eksperimen dengan mengedit button "Informasi Selengkapnya" seperti menambahkan hover dan animasi transisi

---

### 2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan penjelasannya!
#### Jawaban
Elemen h1{...} digunakan untuk mendeklarasi semua elemen h1 yang terdapat di dalam file HTML. Sedangkan, #intro h1 {...}
digunakan untuk mendeklarasi elemen h1 yang berada didalam tag dengan id #intro
```
#intro {
    background: #418fb1;
    border: 1px solid #099249;
    min-height: 100px;
    padding: 10px;
}
#intro h1 {
    text-align: left;
    border: 0;
    color: #fff;
}
```

---

### 3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!
#### Jawaban
Berdasarkan prioritasnya, Inline CSS akan selalu lebih diutamakan, lalu kemudian Internal CSS dan disusul oleh Eksternal CSS <br>
**Inline Css**
```html
        <p style="text-align: center; color: #ccd8e4;">Kami sedang belajar HTML dan CSS dasar, pada mata kuliah <b>Pemrograman Web</b> di
        <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat adalah membuat tampilan web
        sederhana dalam rangka mengenal tag-tag dasar HTML dan CSS</p>
```
**Internal CSS**
```html
    <style>
        body {
            font-family: 'Open Sans', sans-serif;
        }
        header {
            min-height: 80px;
            border-bottom: 1px solid #77ccef;
        }
        h1 {
            font-size: 24px;
            color: #0F189F;
            text-align: center;
            padding: 20px 10px;
        }
        h1 i {
            color: #6d6a6b;
        }
    </style>
```
**Eksternal CSS** <br>
Untuk menyambungkan file HTML dengan file CSS
```html
    <link rel="stylesheet" href="style.css">
```
```css
nav {
    background-color: #20A759;
    color: #fff;
    padding: 10px;
}
nav a {
    color: #fff;
    text-decoration: none;
    padding: 10px 20px;
}
nav .active,
nav a:hover {
    background: #0B6B3A;
}

#intro {
    background: #418fb1;
    border: 1px solid #099249;
    min-height: 100px;
    padding: 10px;
}
#intro h1 {
    text-align: left;
    border: 0;
    color: #fff;
}

.button {
    padding: 15px 20px;
    background: #bebcbd;
    color: #fff;
    display: inline-block;
    margin: 10px;
    text-decoration: none;
    transition: 0.7s;
}
.btn-primary {
    background: #E42A42;
}
.button:hover {
    transition: 0.7s;
    color: #E42A42;
    background: #4c2ae4;
    padding: 20px 25px;
}
```

---

### 4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya! (<p id="paragraf-1" class="text-paragraf">)
#### Jawaban
Jika terdapat id dan class dalam sebuah elemen html, maka id akan selalu di dahulukan. Karena **ID selector** memiliki tingkat prioritas lebih tinggi dibandingkan
dengan **Class Selector**.
```html
<p id="paragraf-1" class="text-paragraf">
```
```css
#paragraf-1 {color: aquamarine;}
.paragraf-1 {color: violet;}
```

---
