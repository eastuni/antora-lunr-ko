# antora-lunr-ko

한국어 검색이 가능하도록 antora 빌드를 하였습니다.

## run script

### antora install

npm i -g @antora/cli @antora/site-generator-default

### node modules

npm i

# npm i ./custom-modules/my-antora-lunr
# npm i ./custom-modules/my-antora-site-generator-lunr
# npm i asciidoctor asciidoctor-kroki
# cp ./custom-modules/lunr-kr/lunr.kr.js node_modules/lunr-languages

### antora build

antora --generator my-antora-site-generator-lunr antora-playbook.yml --attribute DOCSEARCH_ENABLED=true --attribute DOCSEARCH_ENGINE=lunr --attribute DOCSEARCH_LANGS=en,kr --stacktrace

### run web server

npm i -g http-server

http-server public -c-1

## 참고 오픈소스

https://github.com/Mogztter/antora-lunr  
https://github.com/Mogztter/antora-site-generator-lunr  
https://github.com/MihaiValentin/lunr-languages  

  