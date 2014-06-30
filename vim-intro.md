- insert

    i
    a karakterden sonra

- save

    :up
    :w

- save and close

    :wq
    :x
    ZZ


- Yön

    j yukarı
    k aşağı
    h sağ
    l sol


- local config

    ~.vimrc
    set number

- kurulum

    sudo apt-get install vim-full

- help

    :help <CTRL-D>
    :help :wq

- scroll

    Ctrl-f full aşağı
    ctrl-b full yukarı
    ctrl-d yarım aşağı
    ctrl-u yarım yukarı
    ctrl-e tek satır aşağı
    ctrl-y tek satır yukarı

- Kelimeler arası geçiş

    w bir sonraki işaretten sonrasına kadar git (askn.gdk 101 - g'de)word
    W bir sonraki boşluktan sonrasına kadar git (askn.gdk 101 - 1'de)

    e bulunduğu kelimenin sonuna end
    E bulunduğu kelimenin sonuna

    b bir önceki işaretten sonrasına kadar git
    B

- Cursor Pozisyon

    0 satır başı
    $ satır son

- block

    { block başı
    } block sonu

    ( bir önceki cümle
    ) bir sonraki cümle

- Dosya başı/sonu

    :0 başı
    gg

    1G

    G sonu

    :$

- Dosyada gezinme

    20% - dosyanın %20sine git

    :goto 25 - dosyanın 25. karakterine git

- Satır Numarası

    set nu
    set number

    set nonu
    set nonumber

    :50 50.satıra git
    50gg 50 satır yukarı
    50 sağ sol aşağı yukarı
    50 h j k l

- işlem yapılan nokta

    :jumps işlem yapılan noktaları listeler

    Ctrl-O bir öncekine git(belge, bulunulan belge içinde bir nokta)

    Ctrl-I bir sonraki

- Bookmark

    m(isim) kaydet

    ma

    `(isim) git
    `a

- Tüm bookmark'lar

    :marks
    `isim

    :marks a
    ismi a olanın detayını göster

- tag

TODO
    :Tagbar

- İçe alma

dosya içeriğini alma

    :r filename

komut çıktısını alma

    :r! komut


- Replace

    r tek karakter
    R esc'ye basana kadar

- silme

    x karakter
    dw word
    dd satır
    D imlecten satır sonuna
    :%d alayını sil

- swap

    xp swap karakter

- visual

    v karakter
    V satır

    Ctrl-v block

    gv bir önceki seçtiğini bir daha seç

- record

    q ya bas kayda başla
    işlemleri yap
    q ya bas kaydı bitir

    @ bas tekrarla
    3@ 3 kez tekrarla

- sırala

    seç
    :sort
    :sort! tersten sırala

- değişkenin tanımlandığı yer
değişkenin üzerinde iken

    gd

- Split

    :vs
    :sp

ctrl+w değiştirme

    :25 vs deneme

- Tab

    $ vim -p deneme foobar

    :tabc
    :tabclose

    :tabnew belge

    :tabe belge
    :tabedit belge

    :tabs listele
    :tabn sonraki

    :tabn 2

g + t ikilisi ile tablar arası geçiş

README.md

cursoru yazının üzerine getirip

gf eğer bulursa aynı pencerede açar

Ctrl w + f  split olarak açar

Ctrl w + gf tab olarak açar


- map
TODO
- set
TODO

- vim dizin

    :Sex split explore
    :Vex vertical
    :Tex tab
    :Ex

- değiştir

    :%s/_/_/gc
    g hepsi
    c onaylı

- Tamamlama completion

    Ctrl-X Ctrl-P kelime
    Ctrl-X Ctrl-L satır
    Ctrl-X Ctrl-F dosya ismi
    Ctrl-X Ctrl-O dil için

- Yapıştırma

    [yapıştırma](http://vim.wikia.com/wiki/Accessing_the_system_clipboard)

-

    "%p dosya ismini yapıştırır
