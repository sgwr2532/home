##  HTML
~~~
# HTML5 テンプレート
<!doctype html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>タイトル</title>
</head>
<body>
    <!-- ここにコンテンツ -->
</body>
</html>
~~~
~~~
# アクセス制御
 /var/www/html/.htaccess
# HTTPSの使用を強制し、中間者攻撃を防ぐ。
 Strict-Transport-Security: max-age=31536000; includeSubDomains
# クロスサイトスクリプティング（XSS）を防ぎ、許可されたリソースのみを読み込むように制限。
 Content-Security-Policy: default-src 'self'; script-src 'self' trustedscripts.example.com
# クリックジャッキング攻撃を防ぎ、ウェブページが他のページにフレーム化されるのを防ぐ。
 X-Frame-Options: DENY
# MIMEタイプのスニッフィング攻撃を防ぎ、宣言されたコンテンツタイプに従うようブラウザに指示。
 X-Content-Type-Options: nosniff
# XSS攻撃を検出し、ブロックするための設定。
 X-XSS-Protection: 1; mode=block
# リファラーヘッダの情報を制御し、プライバシーを保護。
 Referrer-Policy: no-referrer
~~~
~~~
# CSS

~~~
~~~
# JavaScript

~~~
