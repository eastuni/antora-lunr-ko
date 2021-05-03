# antora-lunr-ko

한국어 검색이 가능하도록 antora 빌드를 하였습니다.

## run script

### antora 설치

`npm i -g @antora/cli @antora/site-generator-default`

### node modules 설치

* 필요시  

`npm i asciidoctor asciidoctor-kroki  `
`npm i  `

### antora build

* powershell
 
`$env:DOCSEARCH_ENABLED='true'; $env:DOCSEARCH_ENGINE='lunr'; $env:DOCSEARCH_LANGS='en,ko'; antora --generator @eastuni/antora-site-generator-lunr-ko antora-playbook.yml --stacktrace`

* shell

`DOCSEARCH_ENABLED=true DOCSEARCH_ENGINE=lunr DOCSEARCH_LANGS=en,kr antora --generator @eastuni/antora-site-generator-lunr-ko antora-playbook.yml --stacktrace`

### run web server

`npm i -g http-server`

`http-server public -c-1`

## 참고 오픈소스

https://github.com/Mogztter/antora-lunr  
https://github.com/Mogztter/antora-site-generator-lunr  
https://github.com/MihaiValentin/lunr-languages  

  