# Завдання №4. Розподілені файлові системи: HDFS, S3 та GCS

## Послідовність виконання завдання


1. Ви маєте залогінитись Google Cloud Platform (далі - GCP). 
2. Створіть проект в GCP для виконання домашніх завдань. Як це зробити, можна прочитати тут. В якості імені проекту виберіть DE-07. В якості ID проекту вкажіть de-07-firstname-lastname. Наприклад: de2023-ivan-ivanenko
3. Для того, щоб почати користуватися GCP, потрібно створити billing account та привʼязати його до проекту.

4. Встановіть консольну утиліту gcloud. 

5. Ви маєте залогінитись в утиліту gcloud. 

6. Знайти сервіс Cloud Storage, створити в ньому бакет. Імʼя бакету може бути довільним, але памʼятайте, що воно має бути глобально унікальним (не лише в межах Вашого проекту).

7. Далі вам потрібно створити пайплайн за допомогою Apache Airflow (локально, докер, або Google Composer), який завантажує AVRO файли. Для цього ви маєте:

* Скачати дані з API з домашки по Python (якщо ви її не робили, то можете скачати через Postman) за 2 дати
* Написати пайплайн, який завантажить ці дані в бакет
* Кожен запуск має завантажити тільки одну дату (взяти з execution_date, Variable, або передати, як параметри запуску)

Примітки:

* Пайплайн має відпрацювати за 2 дати.
* Пайплайн має вантажити файли у бакет за наступним шляхом (приклад для дати 2022-08-01): src1/sales/v1/2022/08/01/
* Ви маєте знайти та використати існуючий оператор. PythonOperator використовувати не бажано
* Якщо маєте бажання, можете використати наступний шлях:  src1/sales/v1/year=2022/month=08/day=01/
