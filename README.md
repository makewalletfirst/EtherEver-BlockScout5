<h1 align="center">Blockscout</h1>
<p align="center">add SC-VERIFIER</p>
<div align="center">
legay solc compiler 추가법 <br>
  docker exec -it backend sh <br>
  cd /app/lib/explorer-9.3.0/priv/solc_compilers/ <br>
  rm v0.6.12+commit.27d51765.js <br>
  wget -O v0.6.12+commit.27d51765.js https://binaries.soliditylang.org/bin/soljson-v0.6.12+commit.27d51765.js <br>
  exit <br>
  docker restart backend <br>
도커 내릴떄마다 새로 맨날 갈겨야함 (자동 추가는 블록스카우트 5부터 적용) 못함 <br>


백엔드에 노드 깔아야함 <br>
docker exec -it backend sh    <br>
# Node.js 설치   <Br>
apk add --no-cache nodejs npm   <br>
<br>
# 설치 확인 (버전이 뜨면 성공) <br>
node -v <br>
<br><br><br>

백엔드에 SOLC 깔아야함<br>
docker exec -it backend sh <br>
# 솔리디티 컴파일러 라이브러리 설치 <br>
npm install solc <br>
<br>
# (혹시 모르니 전역으로도 연결) <br>
npm install -g solc <br>

