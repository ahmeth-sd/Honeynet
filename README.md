# Honeynet Geliştirme Projesi

## Proje Özeti

Bu proje, ağ güvenliği tehditlerine karşı daha etkili bir mücadele stratejisi geliştirmek amacıyla gerçekleştirilmiştir. Öncelikli hedefimiz, ağ güvenliği tehditlerine karşı koruma sağlamak için özelleştirilmiş bir honeynet sistemi geliştirmektir. Honeynet, gerçek bir ağ ortamını taklit eden ve saldırganları kendisine çekmek amacıyla sistematik olarak tasarlanmış bir kısım olan honeypot'larla oluşturulan bir ağ topolojisidir.

## Honeypotlar

Bu projede, farklı tür honeypot'ları entegre eden bir honeynet ağı tasarlanmıştır ve uygulanmıştır. Honeypot'lar, sahte servisler, açık portlar, zayıf güvenlik önlemleri gibi gerçek bir ağ ortamını taklit eden yapılar olarak oluşturulur. Bu yapılar, saldırganların dikkatini çekmeyi amaçlar ve onları ağdaki kritik kaynaklardan uzaklaştırır. Saldırganlar honeypot'lara saldırdıkça, onların hareketleri izlenir ve kaydedilir. Bu bilgiler, saldırganların hedeflediği zayıf noktaları, saldırı vektörlerini ve kullanılan araçları belirlemek için analiz edilir.

## Kullanılan Araçlar

Bu projede [Dionaea](https://dionaea.readthedocs.io/en/latest/index.html), [Cowrie](https://github.com/cowrie/cowrie), [Elastichoney](https://github.com/jordan-wright/elastichoney) gibi farklı honeypotlar ve [ELK Stack](https://www.elastic.co/elastic-stack?ultron=B-Stack-Trials-EMEA-S-PHS&gambit=Stack-ELK&blade=adwords-s&hulk=paid&Device=c&thor=elk%20stack) ile [Power BI](https://powerbi.microsoft.com/tr-tr/) gibi log analiz ve görselleştirme araçları kullanılmıştır. Bu araçlar sayesinde, saldırganların hareketleri ve taktikleri hakkında detaylı bilgiler elde edilmiş ve bu bilgiler, proaktif güvenlik önlemleri alınmasını kolaylaştırmıştır.

## Analiz ve Sonuçlar

Honeypotlar üzerine gelen saldırılar ve bu saldırılardan elde edilen verilerin analizi sonucunda saldırganların taktiklerini, tekniklerini ve prosedürlerini daha iyi anlama imkanı sağlandığı görülmüştür. Bu bilgiler ışığında proaktif güvenlik önlemleri alınması kolaylaşmıştır.

Bu projede elde edilen verilerin analizi ve görselleştirilmesi ile kullanılan kullanıcı adı parola çiftleri, şüpheli IP adresleri, saldırı gelen protokoller, ülkeler, zararlı hash’ler, payload’lar ve komutlar incelenmiştir.

Honeynet sisteminin yapı taşları honeypot’lardan biri olan Dionaea honeypot üzerine gelen saldırıların bazılarında MD5 Hash değeri elde edilmiştir. Bu hash değerleri VirusTotal üzerinde aratıldığında WannaCry Ransomware zararlı yazılımına ait oldukları görülmektedir.

Gelen bir diğer hash VirusTotal üzerinde aratıldığında zararlı bir yazılım olduğu görüldü. Bu zararlı yazılıma ait IP adresi “210.1.100.39” Cisco Talos Intelligence, AbuseIPDB, LiveIPMap gibi kaynaklarda incelendiğinde sadece AbuseIPDB üzerinde 5 ay önce 1 kere rapor edildiği görülmüştür.

Elastichoney honeypot sisteminin yakaladığı payload değerleri hakkında şu bulgular elde edilmiştir: İlk JSON payload, veritabanı sorgusu olarak belirlendi. İkinci JSON payload, Elastichoney sisteminde belirli Çince ifadeleri içeren bir arama sorgusu oluşturuyor. Üçüncü JSON payload, Elastichoney sisteminde belirli bir zaman diliminde tüm olayları sorgulamak için kullanılıyor. Son XML payload, bir JAMF mesajı oluşturur ve belirli bir cihazı, uygulamayı ve zaman damgasını tanımlar.

## Gelecek Planları

Tehdit aktörlerinin yöntemleri her geçen gün değişmektedir. Gelecekte aynı alanda farklı protokollerde çalışan farklı honeypot’lar üzerinde benzer bir çalışma yapılmasının; siber tehdit istihbaratı sağlamada, tehdit aktörlerinin TTP’lerini anlamada ve bunlara göre önlem almada katkı sağlayacağı değerlendirilmiştir.
