# Cyberwise Weakness Enumeration

CWE alternatifi olarak düşündüğümüz (CWE'de 1003 View'i var ama o da karmaşık), basit ve anlaşılır bir yapıda olmasına çalıştığımız zafiyet enumerasyon projesidir. Kategori ve zayıflık sınıfları vardır. Zayıflıkların alt elemanı olamaz. Her elemanın kodu bulunur (AC, AC-AUTHN gibi). Alt elemanların sonu her türlü zafiyet olacaktır ve zafiyetlere kod bulaamzsak sayı ile ilerleyebiliriz. https://github.com/appsectr/secnet reposundaki json'a ara ara aktarılacaktır. Bu json'un ara ara yedeğinin alınması gereklidir. Yedekler de burada duracaktır. Şu an (22.08.2025) ana kategoriler hazır ancak alt kategoriler, altın değer (max zincir eleman sayısı) vs belli olmadığı için bir kategori altında ya düzenli bir şekilde gidilecek, ya da o kategori altında olabilen her şey (yorumlarla birlikte) konulacaktır.

### Genel Sorular
- SSRF, CSRF (Belki AC-SESSION altında), Open Redirection (ilişkili SCW: Unvalidated Redirects and Forwards), File Upload Vulns nerede karşılanacak?
- CWE-184 (Incomplete List of Disallowed Inputs) nerede karşılanabilir?
- CWE-357 (Insufficient UI Warning of Dangerous Operations) ilginç bir kategoriymiş, eklenebilir.
- CWE-602 (Client-Side Enforcement of Server-Side Security) güzel kategori, eklenebilir.
- CWE Eşleşme oranı çıkarılabilir. Etkili olacaktır.
- CWE-1253 (Incorrect Selection of Fuse Values) NEREYE KOYABİLİRİZ?
- CWE-551 (Incorrect Behavior Order: Authorization Before Parsing and Canonicalization) INJ altına konulabilir mi? AUTHZ'den geldi.