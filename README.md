# SQL_Assignment_5

## Sorgu Senaryoları

* film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en uzun (length) 5 filmi sıralayınız.

```bash
SELECT title, length
FROM film
WHERE title LIKE '%n'
ORDER BY length DESC
LIMIT 5;
```

* film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en kısa (length) ikinci(6,7,8,9,10) 5 filmi(6,7,8,9,10) sıralayınız.

```bash
SELECT title, length
FROM film
WHERE title LIKE '%n'
ORDER BY length ASC
LIMIT 5 OFFSET 5;
```


* customer tablosunda bulunan last_name sütununa göre azalan yapılan sıralamada store_id 1 olmak koşuluyla ilk 4 veriyi sıralayınız.

```bash
SELECT first_name, last_name
FROM customer
WHERE store_id = 1
ORDER BY last_name DESC
LIMIT 4;
```

## Ek Bilgiler:

* LIKE operatörü, bir metin ifadesinin belirli bir örüntüye uyup uymadığını kontrol etmek için kullanılır.
* ORDER BY sorgusu, sonuçları belirli bir sütuna göre sıralamak için kullanılır.
* DESC anahtar sözcüğü, sonuçları azalan sırada sıralamak için kullanılır.
* LIMIT sorgusu, belirli sayıda sonucu döndürmek için kullanılır.
* OFFSET sorgusu, belirli sayıda sonucu atlamak için kullanılır.

