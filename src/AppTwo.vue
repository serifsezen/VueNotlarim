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
                <input
                  type="text"
                  class="form-control"
                  id="username"
                  v-model.trim="userData.username"
                />
              </div>
              <div class="form-group">
                <label for="password">Password</label>
                <input
                  type="password"
                  class="form-control"
                  id="password"
                  v-model.lazy="userData.password"
                />
              </div>
              <div class="form-group">
                <label for="age">Yas</label>
                <input
                  type="text"
                  class="form-control"
                  id="age"
                  v-model="userData.age"
                />
              </div>
              <div class="form-group">
                <label for="explanation">Aciklama</label>
                <textarea
                  id="explanation"
                  rows="3"
                  class="form-control"
                  v-model="userData.explanation"
                ></textarea>
              </div>
              <div class="form-group form-check">
                <input
                  type="checkbox"
                  class="form-check-input"
                  id="exampleCheck1"
                  value="Yazilim"
                  v-model="userData.ilgiAlanlari"
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
                  id="exampleCheck2"
                  value="Donanim"
                  v-model="userData.ilgiAlanlari"
                />
                <label
                  class="form-check-label"
                  style="padding: 5px"
                  for="exampleCheck2"
                  >Donanim</label
                >
              </div>
              <div class="form-check">
                <input
                  class="form-check-input"
                  type="radio"
                  name="flexRadioDefault"
                  id="flexRadioDefault1"
                  value="Erkek"
                  v-model="userData.cinsiyet"
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
                  value="Kadin"
                  v-model="userData.cinsiyet"
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
                <select class="form-control" v-model="userData.seciliSehir">
                  <option v-for="(item,index) in userData.sehir" :key="index">{{item}}</option>
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
            <p>Kullanici Adi: {{ userData.username }}</p>
            <p>Sifre:{{ userData.password }}</p>
            <p>Yas:{{ userData.age }}</p>
            <p style="white-space: pre;"> Aciklama:{{ userData.explanation }}</p>
            <p><strong>ilgi Alanlari:</strong></p>
            <ul>
              <li v-for="(item,index) in userData.ilgiAlanlari" :key="index">{{item}}</li>
            </ul>
            <p>cinsiyet:{{userData.cinsiyet}}</p>
            <p>Sehir:{{userData.seciliSehir}}</p>
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
  data() {
    return {
      userData: {
        username: "",
        password: "",
        age: "",
        explanation: "",
        ilgiAlanlari:[],
        cinsiyet:'',
        sehir:["Antalya","izmir","istanbul","van"],
        seciliSehir:''
      },
    };
  },
};
</script>