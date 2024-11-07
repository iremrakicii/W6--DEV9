Bu README dosyasında SQL veritabanı sorguları yer almakta olup her bir sorgunun işlevi kısaca açıklanmıştır.

### Sorgu Açıklamaları
### 1. Sorgu: Şehir ve Ülke Bilgilerini Birleştirme
Bu sorgu, city ve country tablolarını INNER JOIN ile birleştirerek her bir şehre karşılık gelen ülke adını listeler.

'''sql
SELECT city.city, country.country 
FROM city
INNER JOIN country ON city.city_id = country.country_id;
'''
Açıklama: city ve country tablolarında şehir ve ülke bilgilerini city_id ve country_id değerleri üzerinden eşleştirir ve her şehir için ülke adını döndürür.

### 2. Sorgu: Ödeme ve Müşteri Bilgilerini Listeleme
Bu sorgu, customer ve payment tablolarını INNER JOIN kullanarak birleştirir ve her ödeme kaydına ait müşteri adını ve soyadını getirir.

'''sql
SELECT payment.payment_id, customer.first_name, customer.last_name
FROM customer
INNER JOIN payment ON customer.customer_id = payment.customer_id;
'''
Açıklama: payment tablosundaki her bir ödeme için, ilgili müşteri bilgileri (first_name ve last_name) customer_id üzerinden eşleştirilerek listeye eklenir.

### 3. Sorgu: Kiralama ve Müşteri Bilgilerini Listeleme
Bu sorgu, customer ve rental tablolarını INNER JOIN ile birleştirir ve her kiralama kaydına ait müşteri adını ve soyadını döndürür.

'''sql
SELECT rental.rental_id, customer.first_name, customer.last_name 
FROM customer
INNER JOIN rental ON rental.customer_id = customer.customer_id;
'''
Açıklama: rental tablosundaki her bir kiralama için, ilgili müşteri bilgileri customer_id üzerinden eşleştirilerek kiralama ve müşteri bilgilerini bir arada sunar.

