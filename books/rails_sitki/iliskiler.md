## 1-1

    rails g model CarDetail .... car:belongs_to
    rails g model CarDetail .... car:references

car_id adında indexli bir alan ekler
yabancı anahtarın bulunduğu model belongs_to

    car.rb
    has_one: :car_detail

    car_detail.rb
    belongs_to: :car

## N-M

    class Car
      has_many :rentals
      has_many :customers, through: :rentals
    end
    class Customer
      has_many :rentals
      has_many :cars, through: :rentals
    end
    class Rental
      belongs_to :car
      belongs_to :customer
    end

### Has and belongs to many

Üçüncü modele ihtiyaç duymaz. Yeni alan, validates, geri çağırma metodları kullanılamaz.

## N+1 Problemi

    Make.includes(:cars)
    Car.includes(:make, :rentals)

