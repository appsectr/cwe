### Vulncat karşılığı -> Weak Encryption: Inadequate RSA Padding

### CWE karşılığı -> https://cwe.mitre.org/data/definitions/780.html

### Bizde ise şu an (25.08.2025) CRYPTO-ALGO içinde veya o kategori olursa altında olabilir.

### Ayağa kaldırılabilme durumu: Kaldırılamaz

The product relies on the RSA algorithm without applying Optimal Asymmetric Encryption Padding (OAEP), reducing the overall security of the encryption.

Zafiyetli Kod
```
...
static public byte[] encrypt(byte[] plaintext, RSAParameters rsaParameters) {
    RSACryptoServiceProvider rsa = new RSACryptoServiceProvider();
    rsa.ImportParameters(rsaParameters);
    return rsa.Encrypt(plaintext, false);
}
...
```

Doğrusu
```
...
static public byte[] encrypt(byte[] plaintext, RSAParameters rsaParameters) {
    RSACryptoServiceProvider rsa = new RSACryptoServiceProvider();
    rsa.ImportParameters(rsaParameters);
    return rsa.Encrypt(plaintext, RSAEncryptionPadding.OaepSHA256);
}
...
```