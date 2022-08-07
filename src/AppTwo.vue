<template>
  <h1>Form Verileriyle Calismak</h1>
  <hr />
  <div class="col-md-6">
    <div class="container">
      <div class="panel panel-warning">
        <div class="panel-heading">Basvuru Formu</div>
        <div class="panel-body">
          <form>
            <div class="col-md-12">
              <div class="form-group">
                <label for="username">Kullanici Adi</label>
                <input type="text" class="form-control" id="username" />
              </div>
              <div class="form-group">
                <label for="password">Password</label>
                <input type="password" class="form-control" id="password" />
              </div>
              <div class="form-group">
                <label for="age">Yas</label>
                <input type="text" class="form-control" id="age" />
              </div>
              <div class="form-group">
                <label for="explanation">Aciklama</label>
                <input type="text" class="form-control" id="explanation" />
              </div>
              <div class="form-group form-check">
                <input
                  type="checkbox"
                  class="form-check-input"
                  id="exampleCheck1"
                />
                <label
                  class="form-check-label"
                  style="margin-right: 10px; padding: 5px"
                  for="exampleCheck1"
                >
                  Yazilim</label
                >
                <input
                  type="checkbox"
                  class="form-check-input"
                  id="exampleCheck1"
                />
                <label
                  class="form-check-label"
                  style="padding: 5px"
                  for="exampleCheck1"
                  >Donanim</label
                >
              </div>
              <div class="form-check">
                <input
                  class="form-check-input"
                  type="radio"
                  name="flexRadioDefault"
                  id="flexRadioDefault1"
                />
                <label
                  class="form-check-label"
                  style="padding: 10px"
                  for="flexRadioDefault1"
                >
                  Erkek
                </label>

                <input
                  class="form-check-input"
                  type="radio"
                  name="flexRadioDefault"
                  id="flexRadioDefault2"
                />
                <label
                  class="form-check-label"
                  style="padding: 10px"
                  for="flexRadioDefault2"
                >
                  Kadin
                </label>
              </div>
              <div class="form-group">
                <label for="sel1">Sehir</label>
                <select class="form-control" id="sel1">
                  <option>Antalya</option>
                  <option>izmir</option>
                  <option>istanbul</option>
                  <option>van</option>
                </select>
              </div>
              <button type="submit" class="btn btn-primary">Gonder</button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
  <div class="col-md-6">
    <div class="container">
      <div class="panel panel-info">
        <div class="panel-heading">Form Verileri</div>
        <div class="panel-body">
            <div class="col-md-12">
                <p>Kullanici Adi:</p>
                <p>Sifre:</p>
                <p>Yas:</p>
                <p>Aciklama:</p>
                <p><strong>ilgi Alanlari:</strong> </p>
                <ul>
                    <li></li>
                </ul>
                <p>cinsiyet:</p>
                <p>Sehir:</p>
                <p>Toggle:</p>
            </div>
            
        </div>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  components: {},
  setup() {},
};
</script>