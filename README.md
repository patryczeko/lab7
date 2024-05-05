# lab7
Pierwszym krokiem jest zalogowanie się do dockerhuba
```
docker login
```
Następnie musimy zbudować obraz poleceniem
```
docker buildx build -f DockerfileA --platform linux/amd64,linux/arm64 --cache-from=type=registry,ref=<mojeregistry>/cache --cache-to=type=registry,ref=<mojeregistry>/cache,mode=max --tag <mojeregistry>/<nazwarepo> --push .
```
<mojeregistry> zmieniamy na nazwę naszego użytkownika na dockerhubie 

Przy pierwszym użyciu pojawi nam się błąd:

![image](https://github.com/patryczeko/lab7/assets/106553021/e85c3e3a-f152-41ef-a49b-c232c32dbcb9)

Dzieje się tak ponieważ cache jeszcze nie jest nigdzie przechowywany (nie został utworzony), przy drugim użyciu powyższego polecenia wszystko powinno się udać bez problemu 

![image](https://github.com/patryczeko/lab7/assets/106553021/d6201d14-54bc-4a3d-aef6-2302ae16083f)


