# snowpack-url-folders

Repro:

```
git clone https://github.com/lgarron/snowpack-url-folders && cd snowpack-url-folders
npm install

npx snowpack dev

# This works
open http://localhost:8080/example/
# This doesn't work:
open http://localhost:8080/example.com/

# Both of these work:
open http://localhost:8080/example/index.html
open http://localhost:8080/example.com/index.html
```

<http://localhost:8080/example.com/> triggers the following error:

```
[18:19:22] [snowpack] Error: /Users/lgarron/Code/git/github.com/lgarron/snowpack-url-folders/public/example.com/index.html - Requested content ".com" but only built .html
[18:19:22] [snowpack] [500] /example.com/
```
