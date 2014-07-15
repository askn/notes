cars_new_path

    get '/cars/new', to: 'cars#new'

resources

    new_cars_path

Controller içinde _url
View içinde _path

    resources :makes do
      resources :cars # belongs_to :make
    end

## Yüzeysel Rotalar

İhtiyaç olmayan url adresleri için iç içe kullanımı devre dışı bırakır. Yalnızca index, new, create için geçerli olmasını sağlar.

    resources :makes, shallow: true do
      resources :cars
    end

## Member

İlk önce idye göre ilgili car seçilecek

    resources :cars do
      member do
        get 'rent'
      end
    end
    # rent_car GET /cars/.id/rent

    resources :cars do
        get 'rent'
    end
    # car_rent GET /cars/.car_id/rent

    resources :cars do
      get 'rent', on: :member
    end

## Collection

Memberdaki gibi tek tek üyelerle değilde tüm koleksiyon ile kullanmak için

    resources :cars do
      collection do
        get 'find'
      end
    end
    find_cars GET /cars/find

    resources :cars do
      get 'find', on: :collection
    end

## İsimlendirme

    get 'cars', to: 'cars#index', as: :vehicles

## Yönlendirme

    get 'cars', to: 'cars#index'
    get 'cars/list', to: redirect('/cars')

# Türkçeleştirme

    resources :cars, path: 'arabalar'

    scope(path_names: { new: 'yeni', edit: 'güncelle' }) do
      resources :cars, path: 'arabalar'
    end

