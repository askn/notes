## Rails

- 2004 yılı
- 37signals firması
- David Heinemeiner Hansson (DHH)

- Konfigürasyon üzerine kabuller - Convention over Configuration (COC)
- Don't Repeat Yourself (DRY)

## HTTP istek metotları

Get: kaynağı getir
Post: yeni bir kaynak oluştur
Put/Patch: tüm alanların güncellenmesi Put, bazı alanların güncellenmesi Patch
Delete: sil

## Http Durum Kodları

2XX: başarılı
200 OK: istek başarı ile gerçekleştirildi

3XX: Yönlendirme

4XX: İstemci Hatası
400 Bad Request: biçimsel hatalar var
401 Unauthorized: Yetkilendirme hatası
404 Not Found: İstenilen kaynak bulunamadı

5XX: Sunucu Hatası
500 Internal Server Error: Sunucuda beklenmeyen durum

---

Webrick yerine başka sunucu kullanma

    rails server webrick
    rails server mongrel

## MVC

Model: uygulamada kullanılan verilerin yaşadığı bölüm
Controller: Gelen istekleri gerçekleştirmek üzere gerekli görevleri yerine getiren bölüm
View: Arayüz

## Gemfile

    gem 'rails', '4.0.0.rc2' kesin bu sürüm kullanılacak
    gem 'rails', '>= 4.0.0'
    gem 'rails', '~> 4.0.0' son basamak değişebilir demek

    gem 'foo', group: :development
    gem 'foo', group: [:test, :development]
    group :test do
        gem 'foo'
    end

## Yeni Proje

    rails new isim

bundler çalıştırmadan oluştur

    rails new isim -B
    rails new isim --skip-bundle

testleri oluşturma

    rails new isim -T

## Gemfile.lock

paketler ve version numaralarını içerir
herkesin aynı paket ve sürümleri kullanması için gerekli

Kullanılan paketlerin güncellenmesi

    bundle update
    bundle update paket

Kullanılan paketlerin yeni versiyonları olup olmadığını kontrol eder

    bundle outdated

## Bundle Exec ve Binstubs

    rake --version
    rake, version 10.0.4

    bundle exec rake --version
    rake, version 10.1.0

bundle exec ile uygulamada belirtilen sürüm kullanılır
bundle exec yerine

    bin/rake
    bin/rails server

bin klasörü yoksa oluştur

    bundle exec rake rails:update:bin

## Rake

Görevleri listele

    rake --tasks
    rake -T

    rake -T test

    rake about
    uygulama hakkında bilgiler

    rake notes
    TODO, FIXME.. vs
