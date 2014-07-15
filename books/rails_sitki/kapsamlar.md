    def self.kiralanmamis
      where(rented: false)
    end

    scope :kiralanmamis, -> {where(rented: false)}
    scope :kiralanmamis, proc {where(rented: false)}

    scope :model, ->(year) {where(year: year)}

    default_scope {where(rented: false)}
    default_scope {kiralanmamis}

Sınıf metodları ile kapsamın farkı: kapsamın zincirleme kullanılabilmesi
sınıf metodları bazen kullanılamaz

Kapsamlar her zaman geriye ActiveRecord::Relation nesnesi döndürür
