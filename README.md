# Flight Radar — Redux Toolkit + Thunk

Bu proje, gerçek zamanlı uçuş verilerini listeleyen ve harita üzerinde gösteren küçük bir React uygulamasıdır. Vite, React ve Redux Toolkit (thunk ile) kullanılarak geliştirilmiştir. Proje, uçak ve havalimanı detaylarını modal pencerelerde gösterir ve resim galerisi/süre gibi yardımcı bileşenler içerir.

## Özellikler

- Uçuş listesini getirir ve sayfalandırır
- Harita üzerinde havalimanı/veya uçak işaretleri
- Uçak / havalimanı detay modal'ları
- Galeri ve zaman bileşenleri
- Redux Toolkit ile merkezi durum yönetimi (slices: `flight-slice.js`, `detail-slice.js`)

## Teknolojiler

Aşağıda projenin `package.json` içindeki bağımlılıkları listelenmiştir.

### Kütüphaneler (dependencies)

- @reduxjs/toolkit
- @splidejs/react-splide
- @tailwindcss/vite
- axios
- leaflet
- lucide-react
- react
- react-dom
- react-leaflet
- react-paginate
- react-redux
- react-router-dom
- tailwindcss


## Proje Yapısı (ana dosyalar)

src/

- App.jsx — uygulama kökü
- main.jsx — Vite giriş noktası
- index.css — temel stiller
- components/ — yeniden kullanılabilir bileşenler (header, loader, modal, vs.)
- pages/
  - list/ — uçuş listesi sayfası
  - map/ — harita sayfası ve marker bileşenleri
- redux/
  - store.js — Redux store
  - slices/ — `flight-slice.js`, `detail-slice.js`
  - actions/ — ek action'lar (gerekirse)
- utils/
  - api.js — API çağrıları için axios instance / helper'lar
  - constants.js, helpers.js — yardımcı sabitler ve fonksiyonlar

Bu proje yapısı, komponent bazlı geliştirme ve Redux Toolkit kullanımını yansıtır. Yeni bir bileşen veya sayfa eklerken ilgili klasöre küçük, tek sorumluluklu dosyalar eklemeye çalışın.

## Çalışma mantığı kısa notlar

- Uçuş verisi `flight-slice` içinde asenkron thunk ile çekilir.
- Detay görüntüleme `detail-slice` üzerinden yönetilir (modal aç/kapa).
- Harita işaretleri `map` sayfasında `react-leaflet` ile render edilir.


## Kaynaklar

- API örneği: https://rapidapi.com/apidojo/api/flight-radar1 (kullanılan veya referans alınan API)


![shot](/public/shot.jpg)




<br>


![shot](/public/shot2.jpg)


<br>



![shot](/public/shot3.jpg)



<br>




![gif](/public/gif-1.gif)