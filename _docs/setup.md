## 최초 생성(windows)

### local sites

"""
name: wp-test-site-udemy-wordpress-developer
user: jnjsoft.web
email: jnjsoft.web@gmail.com
github: jnjsoftweb
"""

### files

### folder.file 삭제, 복사

```sh
cd "C:\Users\Jungsam\Local Sites\wp-test-site-udemy-wordpress-developer\app\public"
rmdir /s /q "wp-content\themes\twentytwentythree"
rmdir /s /q "wp-content\themes\twentytwentytwo"

xcopy "C:\Users\Jungsam\Local Sites\_template\basic\*" "C:\Users\Jungsam\Local Sites\wp-test-site-udemy-wordpress-developer\app\public\" /s /e /h /y
```

### file replace strings

```
wp-test-site-udemy-wordpress-developer
UDEMY Become a WordPress Developer: Unlocking Power With Code
jnjsoft.web
jnjsoft.web@gmail.com
jnjsoftweb
```

### github

```sh
github -e pushRepo -u jnjsoftweb -n wp-test-site-udemy-wordpress-developer -d "UDEMY Become a WordPress Developer: Unlocking Power With Code"
```

### vscode 작업영역에 폴더추가

"/Users/youchan/Local Sites/wp-test-site-udemy-wordpress-developer/app/public/"

## 최초 생성(macos)

### local sites

"""
name: wp-test-site-udemy-wordpress-developer
user: jnjsoft.web
email: jnjsoft.web@gmail.com
github: jnjsoftweb
"""

### files

### folder.file 삭제, 복사

```sh
cd "/Users/youchan/Local Sites/wp-test-site-udemy-wordpress-developer/app/public"
rm -rf "wp-content/themes/twentytwentythree"
rm -rf "wp-content/themes/twentytwentytwo"

cp -R "/Users/youchan/Local Sites/_template/basic/". "Users/youchan/Local Sites/wp-jnjsoft-learn/app/public/"
```

# copy

## local sites

"""
name: wp-test-site-udemy-wordpress-developer
user: jnjsoft.web
password:
email: jnjsoft.web@gmail.com
"""

## copyRepo

```sh
cd "C:\Users\Jungsam\Local Sites\wp-test-site-udemy-wordpress-developer\app"

# delete C:\Users\Jungsam\Local Sites\wp-test-site-udemy-wordpress-developer\app\public\wp-content\themes\twentytwentythree
rmdir /s /q "public\wp-content\themes\twentytwentythree"
rmdir /s /q "public\wp-content\themes\twentytwentytwo"

# github copy remote repository
github -e copyRepo -u jnjsoftweb -n wp_wp-test-site-udemy-wordpress-developer

# move github local repository
xcopy "C:\Users\Jungsam\Local Sites\wp-test-site-udemy-wordpress-developer\app\wp_wp-test-site-udemy-wordpress-developer\*" "C:\Users\Jungsam\Local Sites\wp-test-site-udemy-wordpress-developer\app\public" /s /e /h /y
```

## composer(dotenv)

### php 설치 폴더 확인

phpinfo();

"""
Loaded Configuration File C:\Users\Jungsam\AppData\Roaming\Local\run\Mn-mNyiYX\conf\php\php.ini
"""

> `C:\Users\Jungsam\AppData\Roaming\Local\run\Mn-mNyiYX\conf\php\php.ini`

```ini
extension_dir="C:/Users/Jungsam/AppData/Roaming/Local/lightning-services/php-8.1.29+0/bin/win64/ext"
```

> `C:\Users\Jungsam\AppData\Roaming\Local\lightning-services\php-8.1.29+0\bin\win64\php.exe`

### composer 설치(windows10)

- 다운로드
  https://nam24.tistory.com/23
- Setup 파일 실행
  Composer Setup
  - php 경로: C:\APM\php8\php.exe

### dotenv

> `C:\Users\Jungsam\Local Sites\wp-test-site-udemy-wordpress-developer\app\public\_env\.env`

```
ADMIN_USER_ID=
ADMIN_USER_PW=
ADMIN_USER_EMAIL=
MYSQL_IP=
MYSQL_PORT=
MYSQL_ID=
MYSQL_PW=
MYSQL_DB=
```

```sh
cd "C:\Users\Jungsam\Local Sites\wp-test-site-udemy-wordpress-developer\app\public\_env"
composer require vlucas/phpdotenv
```

## check in browser

"""
http://wp-test-site-udemy-wordpress-developer.local/\_test/env.php

http://wp-test-site-udemy-wordpress-developer.local/\_test/mysql.php
"""
