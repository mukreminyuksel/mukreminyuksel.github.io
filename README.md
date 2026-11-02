# Kök site (`mukreminyuksel.github.io`) — doğrulanmış bağlantılar

Bu klasör ayrı ve herkese açık `mukreminyuksel/mukreminyuksel.github.io` deposunun içeriğidir (GitHub Pages kullanıcı
sitesi; adres `https://mukreminyuksel.github.io/`). Tek görevi Android'in **doğrulanmış bağlantılar** (App Links) için
istediği `.well-known/assetlinks.json` dosyasını alan adının kökünde yayımlamaktır. Uygulama (v0.13 ve sonrası,
`app.config.js`) davet ve kişi sayfalarını (`/ilaw-site/davet…`, `/ilaw-site/kisi…`) doğrudan açar. Dosya yoksa ya da
tutmazsa bağlantılar eskisi gibi tarayıcıda açılır.

| Dosya | Görev |
| --- | --- |
| `.well-known/assetlinks.json` | paket `com.mukreminyuksel.ilaw` + gizli imza anahtarının SHA-256 parmak izi (`signing/README.md`; açık bilgi) |
| `.nojekyll` | GitHub Pages noktalı klasörü (`.well-known`) yayımlasın |
| `index.html` | kök adres `ilaw-site`'a yönlenir |

Kurulum ve denetim: docs/SUNUCU.md §0b/10 (operasyon). Play App Signing'de mevcut anahtar kullanılırsa parmak izi değişmez;
Google yeni anahtar üretirse Play Console'daki parmak izi de bu listeye eklenir.
