## 1-1

    rails g model CarDetail .... car:belongs_to
    rails g model CarDetail .... car:references

car_id adında indexli bir alan ekler
yabancı anahtarın bulunduğu model belongs_to

    car.rb
    has_one: :car_detail

    car_detail.rb
    belongs_to: :car


