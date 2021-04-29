# antora-lunr-ko

한국어 검색이 가능하도록 antora 빌드를 하였습니다.

## run script

### antora 설치

`npm i -g @antora/cli @antora/site-generator-default`

### node modules 설치

* 커스텀 모듈 설치

`npm i ./custom-modules/my-antora-lunr  `
`npm i ./custom-modules/my-antora-site-generator-lunr  `

* 한국어 파일 추가  

`cp ./custom-modules/lunr-kr/lunr.kr.js node_modules/lunr-languages ` 

* 필요시  

`npm i asciidoctor asciidoctor-kroki  `
`npm i  `

### antora build

* powershell
 
`$env:DOCSEARCH_ENABLED='true'; $env:DOCSEARCH_ENGINE='lunr'; $env:DOCSEARCH_LANGS='en,kr'; antora --generator my-antora-site-generator-lunr antora-playbook.yml --stacktrace`

* shell

`DOCSEARCH_ENABLED=true DOCSEARCH_ENGINE=lunr DOCSEARCH_LANGS=en,kr antora --generator my-antora-site-generator-lunr antora-playbook.yml --stacktrace`

### run web server

`npm i -g http-server`

`http-server public -c-1`

## 참고 오픈소스

https://github.com/Mogztter/antora-lunr  
https://github.com/Mogztter/antora-site-generator-lunr  
https://github.com/MihaiValentin/lunr-languages  

  