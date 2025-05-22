![Experiment 1.2: sentence after spawner.spawn](image.png)
Output:
```
Arief's Komputer: hey hey
Arief's Komputer: howdy!
Arief's Komputer: done!
```
"hey hey" di print pertama walaupun berada setelah ```spawner.spawn``` disebabkan karena statement println tersebut merupakan statement synchronous biasa pada main, yang akan secara langsung dieksekusi setelah cargo run. Sementara, "howdy!" dan "done!" berada pada block async, yang tidak di run sebelum disuruh oleh executor. Saat block async di run, "howdy!" akan di print terlebih dahulu dan "done!" akan di print 2 detik setelahnya sesuai dengan durasi yang ada di kode.