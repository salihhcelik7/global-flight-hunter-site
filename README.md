# landing/ — Global Flight Hunter tanıtım sayfası

Travelpayouts (ve benzeri affiliate programların) başvuru doğrulamasında
istediği "gerçek, erişilebilir bir site" gereksinimi için hazırlanmış tek
dosyalık statik sayfa.

- `index.html` — sayfanın tamamı. Harici bağımlılık yok (yalnız Google Fonts).
  CSS ve JS gömülü, çerez yok, analitik yok, form yok, kişisel veri toplamıyor.
- `.nojekyll` — GitHub Pages'in Jekyll işlemesini atlaması için (alt çizgiyle
  başlayan dosyalar bozulmasın diye standart uygulama).

## Neden GitHub Pages

Vercel, Cloudflare Pages ve Netlify bu oturumun çalıştığı ağdan erişilemiyor;
ayrıca hiçbirinin CLI'ı kurulu değil. GitHub erişilebilir ama senin kendi
hesabınla kimlik doğrulaması gerekiyor — bunu senin yapman gerekiyor, ben
senin kimlik bilgilerini istemem ve kullanmam.

Üçü de ücretsizdir. GitHub Pages'i öneriyorum çünkü depo zaten sende olacak.

## Yayınlama (~3 dakika)

GitHub'da `global-flight-hunter-site` adında **public** boş bir depo aç
(README ekleme, boş bırak). Sonra:

```powershell
cd D:\GLOBAL-FLIGHT-HUNTER\landing
git init
git add .
git commit -m "Global Flight Hunter landing page"
git branch -M main
git remote add origin https://github.com/<KULLANICI_ADIN>/global-flight-hunter-site.git
git push -u origin main
```

Ardından depo sayfasında: **Settings → Pages → Source: Deploy from a branch →
Branch: `main` / `(root)` → Save.**

1–2 dakika içinde adres yayına girer:

```
https://<KULLANICI_ADIN>.github.io/global-flight-hunter-site/
```

Tarayıcıda aç ve gerçekten açıldığını gör; Travelpayouts başvurusuna
vereceğin URL budur.

## Sonradan güncelleme

Dosyayı düzenle, sonra:

```powershell
git add . && git commit -m "landing güncelleme" && git push
```

## Affiliate marker

`index.html` dosyasının en sonunda, `</footer>` etiketinden hemen sonra bir
HTML yorumu var. Travelpayouts başvurun onaylandıktan sonra verecekleri
doğrulama betiği oraya eklenir.

**Önemli:** Sayfadaki gizlilik beyanı "hiçbir üçüncü taraf betiği
yüklenmiyor" diyor. Bir betik eklediğin anda bu cümle doğru olmaktan çıkar —
beyanı da güncelle.

## Sayfadaki dürüstlük kararları

Başvuru incelemesinde geri tepmemesi için bilinçli olarak:

- Hero'daki fiyatlar `Örnek senaryo — gerçek fiyat değil` etiketi taşıyor.
- "Uygulama geliştirme aşamasındadır, henüz yayında değil ve bilet satışı
  yapmıyoruz" ifadesi görünür bir blok olarak duruyor.
- Sahte App Store / Google Play rozeti, sahte kullanıcı sayısı, sahte yorum yok.
- Uluslararası inceleyiciler için kısa bir İngilizce "About" bölümü var.

---

## YAYINDA (6 Eylül 2026)

**https://salihhcelik7.github.io/global-flight-hunter-site/**

- Repo: https://github.com/salihhcelik7/global-flight-hunter-site (public)
- Yayımlanan dosyalar: **yalnızca** `index.html` + `.nojekyll`.
  Bu `README.md`, backend, docs, mobile, `.env` — hiçbiri public değil.
- HTTPS zorunlu (`https_enforced: true`).

### Güncelleme

`D:\GLOBAL-FLIGHT-HUNTER\landing\index.html` dosyasını düzenledikten sonra
bana söyle, aynı yoldan yayına alırım. Ya da kendin:

```powershell
git clone https://github.com/salihhcelik7/global-flight-hunter-site.git
# index.html'i değiştir
git add . && git commit -m "guncelleme" && git push
```
