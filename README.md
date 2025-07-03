<h1 align="center">CSS Ödevi | Login ve Kayıt Sayfalarını Tasarlama</h1>
<h6 align="center"> [Bu repo, Insider&Testinium Tech Hub Developer Bootcamp ödevi için yapılmıştır.]</h6>

![login](https://github.com/user-attachments/assets/dd3b5cae-df84-493f-bc54-1ee055f4eb9d)
![signup](https://github.com/user-attachments/assets/e3b769a8-83e9-455d-9209-7ad9bc759c9a)

# Amaç: 
İlk gün hazırladığımız login.html ve signup.html sayfalarını ([first-homework](https://github.com/rukenerpolat/first-homework)), CSS bilgileriyle modern ve kullanışlı bir tasarıma kavuşturmak.

![second-homework](https://github.com/user-attachments/assets/fc4e0681-28e8-4706-b7cb-614c721d028a)


## ```Done:``` Genel Kurulum 
- Proje klasörünüzde style.css adında tek bir CSS dosyası oluşturun.
- Bu style.css dosyasını hem login.html hem de signup.html dosyalarınıza ```<link>```
etiketi ile bağlayın. 

#### ```Done:``` 1. Sayfa Arka Planı ve Ortalama
- ```<body>``` etiketini seçerek tüm sayfanın arka plan rengini <b><em>soluk bir gri veya mavi tonu</em></b>
yapın.
>mavi tonları istenince, burada insider renklerini kullanmak istedim ve 
tasarımıma bu maddede karar verdim. 
insider login sayfasına benzer bir tasarım yaptım.

```
:root {
    --color-white: #FFFFFF;
    --color-dark: #18181B;
    --color-dark-grey: #ccc;
    --color-blue: #0A2ECC;
    --color-light-blue: #F3F8FF;
} 
```

#### ```Done:``` 2. Form Kutusu
- Formu sayfada dikey ve yatay olarak ortalayın.
- ```<form>``` etiketlerinizi bir div içine alın ve bu div'e ```.form-container``` gibi bir class verin. 
- Bu ```.form-container```'a stil verin:
   - Beyaz bir background-color ayarlayın.
   - İçeriden boşluk vermek için padding kullanın.
   - Köşeleri yumuşatmak için border-radius ekleyin.
   - Kutuyu sayfadan ayırmak için box-shadow ile hafif bir gölge verin.

```
.form-container {
    background-color: var(--color-white);
    padding: 40px;
    border-radius: 10px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    width: 100%;
    max-width: 400px;
}
```

#### ```Done:``` 3. Başlıklar ve Metinler
"Giriş Yap" ve "Hesap Oluştur" ana başlıklarının yazı tipini ve rengini değiştirin.
```
@import url('https://fonts.googleapis.com/css2?family=Figtree:ital,wght@0,300..900;1,300..900&display=swap');

body kısmında 'font-family: "Figtree", sans-serif;' verildi tüm forma ve h1:

h1,
p {
    color: var(--color-dark);
}
```
Form altındaki "Hesabın yok mu? Kayıt Ol" gibi linklerin altındaki çizgiyi kaldırın ve
rengini değiştirin.

```
ilgili 'a' etiketine class="page-link" verdim ve :hover efekti de ekledim:

.page-link {
    color: var(--color-blue);
    text-decoration: none;
    padding: 10px 0;
    position: relative;
}

.page-link::after {
    background-color: var(--color-blue);
    content: "";
    position: absolute;
    bottom: 5px;
    left: 0;
    width: 0;
    height: 1px;
    transition: width 0.3s ease-in, opacity 0.3s ease-in;
}

.page-link:hover::after {
    width: 100%;
}
```

#### ```Done:``` 4. Form Elemanları   
Tüm input alanlarına (text, email, password) stil verin:
- Genişliklerini %100 yaparak kutuya tam yayılmalarını sağlayın.
- padding ile içten boşluk vererek daha okunaklı hale getirin.
- margin-bottom ile her bir input'un altına boşluk bırakarak birbirlerine
yapışmalarını engelleyin.
- border stillerini değiştirerek daha modern bir görünüm kazandırın.
```
input[type="text"],
input[type="email"],
input[type="password"] {
    width: 100%;
    margin: 5px 0;
    padding: 12px;
    margin-bottom: 10px;
    border: 1px solid var(--color-dark-grey);
    border-radius: 5px;
    box-sizing: border-box;
}

input[type="text"]:focus,
input[type="email"]:focus,
input[type="password"]:focus {
    border-color: var(--color-blue);
    outline: none;
}
```

"Giriş Yap" / "Kayıt Ol" butonlarına özel stil verin:
- Arka plan rengini (background-color) ve yazı rengini (color) değiştirin.
- Varsayılan kenarlığı (border) kaldırın.
- Butonun üzerine gelince imlecin el işareti olmasını sağlayın.

```
button[type="submit"] {
    background-color: var(--color-blue);
    color: var(--color-white);
    width: 100%;
    padding: 12px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-weight: bold;
    transition: background-color 0.2s;
}

button[type="submit"]:hover {
    background-color: rgb(48, 82, 234);
}
```

# Bonus:
```Done:``` Farenizle butonun üzerine geldiğinizde arka plan renginin hafifçe değişmesini
sağlayın.   
```Done:``` Bir input alanına tıklandığında kenarlık renginin (border-color) belirginleşmesini
sağlayın.   
```Done:``` fonts.google.com adresinden seçeceğiniz bir yazı tipini projenize ekleyerek
başlıklarınızda kullanın.   

-----------


<b><em>İncelediğiniz için teşekkür ederim... <br>
Ruken ERPOLAT </em></b>

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-827a67?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/rukenerpolat)
[![Medium](https://img.shields.io/badge/-Medium-827a67?style=flat&logo=medium&logoColor=white)](https://medium.com/@rukenerpolat)