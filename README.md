## install phpseclib/phpseclib

composerを利用してphpseclib/phpseclibを読み込みます
```

composer require phpseclib/phpseclib:~2.0

```

## add BlowfishEncrypter.php

BlowfishEncrypterクラスを新規作成します
App\BlowfishEncrypter

## add AppServiceProvider

App\Providers\AppServiceProvider

encrypterへの再バインドを行います


## check

curlでリクエストを送りHTTPヘッダーを取得して確認します

```

curl -I http://127.0.0.1:8000/
HTTP/1.1 200 OK
Host: 127.0.0.1:8000
Date: Sun, 05 Jul 2020 04:17:00 GMT
Connection: close
X-Powered-By: PHP/7.4.4
Content-Type: text/html; charset=UTF-8
Cache-Control: no-cache, private
Date: Sun, 05 Jul 2020 04:17:00 GMT
Set-Cookie: XSRF-TOKEN=%1B%BD%C3H%80%00m%9F%90%D4%CC%BEeH%3Fe%12%D6%26%92%3B%84%5E%0FX%C8t%0F%A31%A6%85qc%0F%85N3%02%00%03%CE%E1%8D%B6%82BD; expires=Sun, 05-Jul-2020 06:17:00 GMT; Max-Age=7200; path=/; samesite=lax
Set-Cookie: laravel_session=N%0D%93%F2G%E3Q%A9%15~l2%CA9%B8%0FV%E8%1E%60%F7ABZx%E0%C8o%19wy%A0%D7P%89%F3%FD%D8%B6%DB%92P%E5%CF%89IX%1B; expires=Sun, 05-Jul-2020 06:17:00 GMT; Max-Age=7200; path=/; httponly; samesite=lax

```

参考文献：PHPフレームワーク Laravel Webアプリケーション開発
