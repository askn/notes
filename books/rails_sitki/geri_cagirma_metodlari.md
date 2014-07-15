ActiveRecord nesnelerinin oluşturulması, güncellenmesi, kaydedilmesi geçerlilik ilkelerinin denetlenmesi vb. işlemlerin öncesinde veya sonrasında kullanılır.

| Oluşturma | Güncelleme | Yoketme |
| --- | --- | --- |
| before_validation | before validation | before_destroy |
| after_validation | after_validation | around_destroy |
| before_save | before_save | after_destroy |
| around_save | around_save ||
| before_create | before_update ||
| around_create | around_update ||
| after_create | after_update ||
| after_save | after_save ||

### Diğer Callback'ler

- after_initialize

new metodu ile nesne oluşturulunca veya var olan kayıt veri tabanından yüklenmesi sırasında çalıştırılır.Dikkatli kullanılmalı.

- after_find

veri tabanından kaydın yüklenmesi sırasında

- after_touch

- after_commit

bir kaydın eklenemsi, silinmesi, güncellenmesi sonrasında

- after_rollback

hata sonrası geri alma işleminden hemen sonra

    after_save :foo
    def foo
      // kod
    end

    after_save do
      // kod
    end

    after_save :foo, on: :create
