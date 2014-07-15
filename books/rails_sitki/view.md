    render :eylem
    render action: :eylem

    render 'controller/action'

    render file: 'app/views/test/deneme'
    render text: 'test'

Eğer erb etiketleri kullanacaksak

    render inline: '<%= test %>'

    render nothing: true
    render nothing: true, status: 404

    render xml: @cars
    render json: @cars

    render layout: 'test'
    render :index, layout: false

    render status: 404
    render status: :not_found

---

    redirect_to cars_path
    redirect_to 'http://foo.fo'

    redirect_to :back

---

Gövdesi olmayan yanıt mesajları

    head :forbidden
    head 404

---

    <%= render partial: 'list', locals: {cars: @cars, header: 'Arabalar'} %>
