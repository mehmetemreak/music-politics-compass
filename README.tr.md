[🇹🇷 Türkçe](README.tr.md) | [🇬🇧 English](README.md)

# Off Key

**Müzisyenlerin politik pusulası**; söyledikleri ve yaptıkları üzerinden konumlandırılmış, belirsizlik payları ise grafiğe doğrudan işlenmiştir.

**[Grafiği Aç →](https://www.google.com/search?q=https://mehmetemreak.github.io/offkey-politics-compass/)**

Woody Guthrie'den Kneecap'e 191 müzisyen. Her konumlandırmanın yazılı bir gerekçesi ve en az bir kaynağı bulunur; bunları okumak için grafikteki herhangi bir isme tıklayın. Son kapsamlı denetim: 11 Kasım 2026 ([kayıtlar](https://www.google.com/search?q=METHODOLOGY.md%23audits-done)).

## Gruplar değil, kişiler

Bir müzik grubunun tek bir fikri olamaz. Roger Waters ve David Gilmour aynı albümleri yazdı ama çoğu konuda taban tabana zıtlar; John Lydon da Joe Strummer değildir. Dolayısıyla her işaret tek bir kişiyi temsil eder ve aynı grubun üyeleri pusulada birbirinden çok uzak noktalarda yer alabilir.

## Eksenler neyi ölçüyor?

Bu grafik [Political Compass](https://www.politicalcompass.org)'ın testini veya oradaki yerleşimleri değil, yalnızca iki eksenini ödünç alır; nitekim bu çerçevenin [bilinen eleştirmenleri](https://en.wikipedia.org/wiki/The_Political_Compass) mevcuttur. Buradaki otorite ekseni **Coercion (Cebir / Zorlama)** üzerinden tanımlanır: Bir kişinin devletin veya örgütlü bir yapının başkalarına neyi zorla dayatmasını istediği.

|  | Dikkate alınır | Dikkate alınmaz |
| --- | --- | --- |
| **Ekonomik** (sol–sağ) | Vergiler, ücretler, sendikalar, kamu hizmetleri, mülkiyet, piyasalar | Ekonomik kanıt niteliği taşımayan hayır işleri; kişisel vergi planlamaları; kendi telif hakkını savunmak |
| **Otorite** (özgürlükçü–otoriter) | Sansür, kolluk faaliyetleri, uyuşturucu yasaları, göç denetimi, idam cezası, tek parti rejimlerine verilen destek; birinin görüşleri nedeniyle işini, platformunu veya sahnesini kaybetmesine yönelik çağrılar. Bireysel silahlanma her iki yönde de sınırlı etkiye sahiptir. | Rahatsız edici/ofansif olmak; "iptal edilmek" (cancelled); politikaları nedeniyle bir devleti veya şirketi boykot etmek; tilki avı gibi eylemlere yönelik yasaklar |
| **Tek başına ikisine de girmeyenler** |  | Birinin bir savaşta, bir siyasi partide, Brexit'te veya Filistin meselesinde hangi tarafta durduğu. Bu tür "kamp sinyalleri" bir konumu yalnızca düşük güvenilirlikle belirleyebilir. |

Eksenler sabit bir içeriği ölçer. İktidarda kim varsa ona muhalif olmak bir duruş değil, mizaçtır; aynı ölçek 1940 için de 2026 için de geçerlidir.

## Kanıtların ağırlığı

Kanıtın ağırlığı türüne değil, sergilenen duruşun kişiye neye mâl olduğuna (**Costly Action**) bakar:

1. **Bedeli ödenmiş eylem:** Üstlenilen resmi görev, hapis, sürgün, yasaklar, yıllar süren örgütlenme çalışmaları, reddedilen paralar.
2. **Kişinin arkasında durduğu sürdürülebilir kamusal üretim:** Mitinglerde bizzat seslendirdiği ve haklarına sahip olduğu şarkılar dahil.
3. **Açık öz-tanımlama** ve somut politika beyanları.
4. **Tekil sinyaller:** Tek bir oy, tek bir destek açıklaması, tekil bir demeç. Yalnızca yön belirtir, asla merkezden çok uzağa yerleştirmez.

Bir karakterin ağzından yazılan şarkı sözleri ve yazarın sonradan reddettiği parçalar hesaba katılmaz. Sessizlik bir duruş değildir. Her eksenin kendi güvenilirlik seviyesi (yüksek, orta, düşük) vardır ve bu durum grafiğe ±1, ±1.5 veya ±2.5 birimlik bir hare (halo) olarak yansıtılır. Karşılaşılan tüm sınır durumlarla birlikte kuralların tamamı **[METHODOLOGY.md](METHODOLOGY.md)** dosyasında yer almaktadır.

## Bir kayıt nasıl görünür?

Tüm veriler [`data.json`](data.json) içinde tutulur, her kişi tek bir nesnedir. John Lydon'ın kısaltılmış kaydı:

```json
{
  "name": "John Lydon",
  "band": "Sex Pistols",
  "econ": 2, "auth": 0.5,
  "ce": 1, "ca": 3,
  "basis": "Defended Brexit and Farage (2017) and voted for Trump (2020), while still talking up a borderless world.",
  "shift": {
    "label": "Pistols, 1977",
    "econ": -3, "auth": -3, "ce": 1, "ca": 1,
    "basis": "Rests mostly on 'Anarchy in the UK', which fails the attribution gate: Lydon says he is \"not an anarchist\"..."
  },
  "sources": [{ "title": "Dazed: Johnny Rotten defends Donald Trump, Brexit and Nigel Farage (2017)", "url": "https://..." }]
}

```

Önceki bir pozisyon `shift` olarak saklanır ve bir okla çizilir; iki uçtan biri düşük güvenilirlikteyse ok kesikli çizgiye döner. Tüm alanlar [METHODOLOGY.md](https://www.google.com/search?q=METHODOLOGY.md%23data) altında açıklanmıştır.

## Müzik zevkiniz

Grafiğin altına bir Last.fm kullanıcı adı girerek en çok dinlediğiniz 1.000 sanatçıdan hangilerinin pusulada yer aldığını ve dinleme geçmişinizin çalma sayılarıyla ağırlıklandırılmış ortalamasının nereye denk geldiğini görün. Bir grubun dinlenme sayısı, pusuladaki üyeleri arasında eşit olarak paylaştırılır. Bu nokta sizin değil, dinlediğiniz müzisyenlerin nerede durduğunu gösterir.

## Aynı fikirde değil misiniz? Eksik biri mi var?

Bir kaynak belirterek Issue açın:

* **[Bir konuma itiraz et](https://www.google.com/search?q=https://github.com/mehmetemreak/offkey-politics-compass/issues/new%3Ftemplate%3Dplacement.yml):** Hangi eksen olduğu, kişinin sizce nerede durması gerektiği ve bir röportaj, beyan, resmi belge veya kayıt linki. Kaynak gösterilmeyen itirazlar kapatılır.
* **[Müzisyen öner](https://www.google.com/search?q=https://github.com/mehmetemreak/offkey-politics-compass/issues/new%3Ftemplate%3Dsuggest.yml):** Kişinin ekonomik ve otorite alanındaki geçmişi, her iddia için bir kaynak.

Her vaka, hangi tarafın lehine olduğuna bakılmaksızın aynı yöntemle incelenir: Bir tarafın konumunu değiştirecek bir durum, ayna simetriğindeki karşı tarafın konumunu da değiştirmelidir.

## Gizlilik

Ziyaretler, çerez (cookie) kullanmayan ve hiçbir kişisel veri toplamayan [GoatCounter](https://www.goatcounter.com) ile sayılır. Last.fm kullanıcı adı yalnızca Last.fm sunucularına gönderilir ve yalnızca kendi tarayıcınızda hatırlanır.

## Yerelde çalıştırma

Derleme (build) adımı ve bağımlılık yoktur. Sayfa `data.json` dosyasını `fetch` ile yükler, bu yüzden dizini yerel bir sunucuyla açmanız yeterlidir:

```sh
git clone https://github.com/mehmetemreak/offkey-politics-compass.git
cd offkey-politics-compass
python3 -m http.server

```

Ardından http://localhost:8000 adresini açın.

## Teşekkür & Kaynaklar

@mcantuzer'in [bir içeriğinden](https://www.google.com/search?q=https://www.instagram.com/p/DfkCZ8VRQhA) esinlenilmiştir. Dinleme verileri: [Last.fm](https://www.last.fm). Geliştirici: [@mehmetemreak](https://github.com/mehmetemreak); faydalı bulduysanız [masraflara destek olabilirsiniz](https://www.google.com/search?q=https://github.com/sponsors/mehmetemreak).

## Lisans

Kod: [MIT](https://www.google.com/search?q=LICENSE). Veri (`data.json` ve tüm `basis` gerekçeleri dahil): [CC BY 4.0](LICENSE-DATA.md). Off Key kaynak gösterilip geri bağlantı (link) verildiği sürece serbestçe kullanılabilir.
