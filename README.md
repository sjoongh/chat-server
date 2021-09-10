### 프로젝트 폴더 생성
- chat-server

- 프로젝트 만들기
chat-server
약관 동의

애널리틱스 해제
>프로젝트 만들기


### Firebase CLI 설치

```bash
npm install -g firebase-tools
```
### Firebase Login
```bash 
firebase login
```

### firebase project list
```bash 
firebase projects:list
```

### Hosting 설정

```bash
firebase init hosting
```
- Use an existing project
- public directory : public
- configure as a spa app: N
- automatic build: N

### Firebase Functions 설정

```bash
firebase init functions
```
- Language: javascript
- Esling: N

### Firebase Database 설정
```bash
firebase init database
```

### Firebase Database 구축
- 콘솔

### 프로젝트 구축
- 참고 소스: https://raw.githubusercontent.com/okachijs/jsframeworkbook/master/2_5_server/functions/index.js
- functions\index\.js

### 테스트 하기
```bash
firebase serve --only functions
```

### Database 
```bash
database.rule.json 파일을

{
  /* Visit https://firebase.google.com/docs/database/security to learn more about security rules. */
  "rules": {
    ".read": true,
    ".write": true
  }
}
 트루로 바꿔주기
```


# API Test

curl -H 'Content-Type:application/json' -d '{"cname": "general"}' http


채널 목록 확인 API

2:24
curl http://localhost:5000/chat-server-dd7d4/us-central1/v1/channels
2:26
초기화 API
curl -H 'Content-Type:applicat/json' -d '{}' http://localhost:5000/chat-server-dd7d4/us-central1/v1/reset


Chat Server API Endpoints
채널 생성: curl -H 'Content-Type:application/json' -d '{"cname": "general"}' http://localhost:5000/{프로젝트ID}/us-central1/v1/channels
채널 목록: curl http://localhost:5000/{프로젝트ID}/us-central1/v1/channels
초기화: curl -H 'Content-Type:application/json' -d '{}' http://localhost:5000/{프로젝트ID}/us-central1/v1/reset