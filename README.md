# Guide Curl

Ceci est un guide pour Curl.

Actuellement, mes tests on été fait avec le Terminal MacOS et Jenkins.

## Résultats de requètes curl

### Failed to connect to localhost port `<number>` - Connection refused

```
mtl@LDumay-MBP ~ % curl -I -u admin:11c377cc838aaa807d5d458c8c361e506c "http://localhost:8888/job/demo/build?token=xC62Lchv86AphD77Mfyg74PEG3P9"

curl: (7) Failed to connect to localhost port 8888: Connection refused
```

### HTTP/1.1 201 Created

```
~ % curl -I -u admin:11c377cc838aaa807d5d458c8c361e506c "http://localhost:8080/job/demo/buildWithParameters?token=xC62Lchv86AphD77Mfyg74PEG3P9&nom=test" 

HTTP/1.1 201 Created
Date: Mon, 25 Apr 2022 10:53:03 GMT
X-Content-Type-Options: nosniff
Location: http://localhost:8080/queue/item/4/
Content-Length: 0
Server: Jetty(9.4.45.v20220203)
```

### HTTP/1.1 405 Method Not Allowed

```
mtl@LDumay-MBP ~ % curl -I -u admin:11c377cc838aaa807d5d458c8c361e506c "http://localhost:8080/job/demo/build?token=xC62Lchv86AphD77Mfyg74PEG3P9&NOM=test"

HTTP/1.1 405 Method Not Allowed
Date: Mon, 25 Apr 2022 10:51:09 GMT
X-Content-Type-Options: nosniff
Content-Type: text/html;charset=utf-8
Expires: Thu, 01 Jan 1970 00:00:00 GMT
Cache-Control: no-cache,no-store,must-revalidate
X-Hudson-Theme: default
Referrer-Policy: same-origin
Cross-Origin-Opener-Policy: same-origin
Set-Cookie: JSESSIONID.84562195=node017fu74upmu7h5y67cslyd3wvq30.node0; Path=/; HttpOnly
X-Hudson: 1.395
X-Jenkins: 2.344
X-Jenkins-Session: 1c3d797b
X-Frame-Options: sameorigin
X-Instance-Identity: MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAiSUkHynq3HOS0LS+TPt/XUx7KXkNKRJs4Id3UVSCUSN8ZbCtdCwCqtqLoP5XfTGliui3hNBamRLqW9R9T52g5ceDO6KH768lgJY4ZwgVHH7AARKUp5dB9G7Pdx/Jh7UoTobknyLNzJazaizo8CJ9fbYoUmexjDqgyJEwvP8jPY4H3m3O7J+cTQWdKi++g2eKILFV4vjDM4N1J9hToz+Nb/eHB0hnQEKpMq6HoUxk1nQ83xYowsngWEExK9/XARpaTQZ0dqNTxxTQAEQgjQSsqDUmY1T4PCEqyGWw8rs8AXLwTQW80Q6HVjNzvvxOGNPBXPSdbM5UvzbrJeNkaOCcKQIDAQAB
Content-Length: 29265
Server: Jetty(9.4.45.v20220203)
```

## Lecture d'un Job Jenkins

```
curl --silent -u admin:11c377cc838aaa807d5d458c8c361e506c http://localhost:8080/job/demo/26/api/json
```

## Check statuts

```
curl -v telnet://127.0.0.1:8080
curl -v telnet://127.0.0.1:22
curl -v telnet://127.0.0.1:80
curl -v 127.0.0.1:22
curl -v 127.0.0.1:80
curl -v 127.0.0.1:8080
curl -s 127.0.0.1:8080
curl -v 127.0.0.1:8080
curl -v 127.0.0.1:80
curl -v 127.0.0.1:29
curl -v 127.0.0.1:8080
curl -v 127.0.0.1:8888
curl -v 127.0.0.1:8080
curl -v --sslv3 127.0.0.1:8080
```