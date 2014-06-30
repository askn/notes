## Git

### gitignore

    **test
    test altındaki tüm alt klasörleride engelle

    !deneme
    kesinlikle dahil et

### checkout

tümünü geri al

    git checkout -f

sadece belgeyi geri al

    git checkout belge

### branch

oluştur

    git branch deneme

listele

    git branch

dala geç

    git checkout deneme

oluştur ve dala geç

    git checkout -b deneme

dala geç birleştir

    git checkout master
    git merge deneme

dalı sil

    git branch -d deneme

birleştirmeden sil

    git branch -D deneme

Uzak sunucu ekleme

    git remote add isim(origin) link

    git push isim dal_ismi

