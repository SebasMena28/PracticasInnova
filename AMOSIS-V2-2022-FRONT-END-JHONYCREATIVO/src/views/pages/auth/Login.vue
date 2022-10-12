<template>
  <main class="main-content main-content-bg mt-0 ps">
    <section>
      <div class="page-header min-vh-75">
        <div class="container">
          <div class="row">
            <div class="col-xl-4 col-lg-5 col-md-6 d-flex flex-column mx-auto">
              <div class="card card-plain mt-8">
                <div class="card-header pb-0 text-start">
                  <h3 class="font-weight-bolder text-info text-gradient">
                   Bienvenido
                  </h3>
                  <p class="mb-0">Ingresa tu email o usuario y tu password para iniciar.</p>
                </div>
                <div class="card-body">
                  <div role="form" class="text-start">
                    <label>Email / Usuario</label>
                    <div class="mb-3">
                      <input
                        type="text"
                        v-model="email"
                        class="form-control"
                        placeholder="Email"
                        aria-label="Email"
                      />
                    </div>
                    <label>Password</label>
                    <div class="mb-3">
                      <input
                        type="password"
                        v-model="password"
                        class="form-control"
                        placeholder="Password"
                        aria-label="Password"
                      />
                    </div>
                   
                    <div class="text-center">
                      <button
                        type="button"
                        class="btn bg-gradient-info w-100 mt-4 mb-0"
                        @click="iniciar()"
                      >
                        Ingresar
                      </button>
                    </div>
                  </div>
                </div>
               
              </div>
            </div>
            <div class="col-md-6">
              <div
                class="oblique position-absolute top-0 h-100 d-md-block d-none me-n8"
              >
                <div
                  class="oblique-image bg-cover position-absolute fixed-top ms-auto h-100 z-index-0 ms-n6"
                  style="
                    background-image: url('data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAoHCBQUFBYSEhQXGBcXFxgaGhgZFBoaGhkhG
                    BkdIxcVGCIaISwjHR4qIRgZJDYkKS0zNzMzGiI6QTgwQCwyMy8BCwsLDw4PHRISHjopISkyPTcyMjcyMjIyOi8vMjoyMjIyMz0yMjI0Mz03MjIyMi8y
                    MjIyMjIyMjIvMjIyMjI6Ov/AABEIAJwBQwMBIgACEQEDEQH/xAAcAAEAAwADAQEAAAAAAAAAAAAABQYHAQMECAL/xABBEAACAQIEAwUEBgcHBQAAAAAB
                    AgADEQQSITEFBkEHEyJRYTJScYEUI0JikaEzQ3JzgpKzJDVUsbLC0hUWNGPB/8QAGQEBAQEBAQEAAAAAAAAAAAAAAAECAwQF/8QAKBEBAQACAQMDAwQD
                    AAAAAAAAAAECESEDEjEEUWETMkEUgeHwIiRx/9oADAMBAAIRAxEAPwDZoiICIiAiIgIiICIiAiIgIiICIiAiIgIiICIiAiIgIiICIiAiIgIiICIiAiIgI
                    iICIiAiIgIiICIiAiIgcRODM85r7QO7ZqGDCsykhqraqpG6qPtEeZ0+Mlsnl06XSy6mWsY0OJhKYriWLJZHxNXzyFwg9PBZB8JxUfiWE8btiqQ82Z8nzv
                    dfkZjv+Hr/AEP47pv2bxEzHlntEbMKWOtY6Csotb94Bpb7w28us0xTfUTcsvh5er0c+ldZR+4iJXIiIgIiICIiAiIgIiICIiAiIgIiICIiAiIgIiICIiAi
                    IgIiICIiAiIgIiIFX5/4o2HwblDZ6hFNT1Ga+Yj1yhreszXkbgC4vEZX/R01DuBpmubInoDY39FM0DtOwjVMEXUX7qorn4WKk/LNf5Sn9mPFEo4l6TkAV1
                    VVJ2zITlX5hj8wPOc8vum30/T7npsrj5a3RoqihEUKqiwVQAAPIAbSE5q5ipYKmrVULq5K5VK3OlybMRcW3+I85J4rBl9RVdGHslTovxU3Vr/eB9LTwYHg
                    dqhxGJYVqxBUNlypTT3aaknLfqbkm56aTpfh4MO3e8ufhmnPnAEwzpWorlpVgSE6IwAJUehBuB0selpdOzLibVcKabm7UWyA/dIBT8NV+CiV/tT4ojvSwqE
                    E07u9vslgAi/G1yR6iS/ZRhCuHq1SNKlSy+oQWJ/mLD5TlPv4e/q25elly8/j+/8AF+iInV8wiIgIiICIiAiJ1s4G5Aubam2p2HxgdkREBERAREQEREBERA
                    REQEREBERAREQEREBERAREQEREDpr0ldSrAFSCCCLgg7gzHuauSa2GZnw6tUoXuMoLPT+6wGpA94fPzOzTi0zljMnboeoy6V3PHsxXhXPuMoqELpVUaDvFJ
                    YW6ZlIJ+d5++I9oWMqKVUpSBGpRTm/mYm3yF/WdvaXwxqeL78lclcAqB7QKIitcW+Bv6zx8g8NavjKbKVy0SKjhtyNgFFt7kTlvLen1pj0b0/q9s8bc8t8o
                    YjGOHqB6dIm7VHBzPc65A2rE+8dPjtLvzbzVT4QlChSoZyykIufIqqlgSTZjfUdPPWXYTHu2/wDTYT9ir/qSd+nhJdPk+p9Tl1ebxJ+F75S5zw2PWyHJWAu1
                    FiMw82U/bX1G3UCWefMicIxVOhS4hTVu7zNapTJzU2Rit3tqt7aNt8Npo/Jfacr5cPxAhW2WvoEby7wD2D94aedpvLD2ebHL3evmrtNbB4qrhhhFqCll8Zrl
                    b5kVtu7Nvatv0li5i5sXCYKnjGplmqCmEphrDNUXNYtbQAA626bTHO01geJYog3B7og+f1FPWXftO/ujBft0P6Dy3GcJ3XlOcpdomHxrClUXuKxPhRnzK/oj
                    WF2+6QD5Xl3nzDw/gWIr0amIoIXWiyhwuri4JDBeoFtbajyl15K7TKlHLQxxapT2Wr7VRPLP1dfX2v2oyw9jHL3XDnnnxuHVqdEYcVc9PPmNUpbxEWtka+0n
                    +V+NfTMJTxbIKfeByVzZguR2Xcge7faZR2wYmnVxOGqUnV0fDXVlIKkZ21BEvnZ9/c1P93X/AKlSS4ztlJle6xHczdqWHo3p4MCvU9+9qS/Mav8Aw6eszqqv
                    FOLMa2WpXCG4y2SkhHSmCQuYel2854OSsGlbG4WjVUMjuMynZgFJsfS4E32jYAZbKFF1AUZaYLlKaU0FlzGx8R2+BsNXWPgm8vLJeAdoeNwT9xi1eqimzJVu
                    tan6Bm1Pwe/xE1vlzmjC45S2HqXZQC1NhlqJf3l8vUXHrKN2p1KTYNXqU7Vu8RKd1U1ENg7isw2vTv4VvqV1kV2Jf+XX/cD+oslkuO1lsulh5l7RcRgcQ+Hq
                    4Eaao/0ghainZ1+r+RHQ3+Mn+SucafEUbwinVpnx0s+bQnwupsMynbbQ/K/o5x5Zp8QoGk1lqLc0qlvYb181OxH/ANAmCUauJ4di7i9OvRaxB2Pmp95GH4gg
                    +UTGZTjyW2X4fTs8XE+IU8PSevWYKiLdifyA8yToB1Jkfy1zLRxmGGIQhco+sViL02Auwb06g9RrMb7QucTjqvd0iRhqbHINu8YfrW9N8o6DXc6Zxxtulyy1
                    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
                    fMCGCBclIHXxFbkubk+0SOthLpE5nO5WtSSEREKREQEREBERAREQEREBERAREQP/Z');
                  "
                ></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <div class="ps__rail-x" style="left: 0px; bottom: 0px">
      <div class="ps__thumb-x" tabindex="0" style="left: 0px; width: 0px"></div>
    </div>
    <div class="ps__rail-y" style="top: 0px; right: 0px">
      <div class="ps__thumb-y" tabindex="0" style="top: 0px; height: 0px"></div>
    </div>
  </main>
</template>
<script>
import axios from '../../../axios.js'
import { mapActions } from 'vuex';
export default {
    
    data() {
        return {
            email:'',
            password:'',
          
            usuario :{}
        }
    },computed:{
        
    },
        methods: {
          ...mapActions(['getAmosisUser']),
            async iniciar(){
                let loader = this.$loading.show();
                 const swalWithBootstrapButtons = Swal.mixin({
customClass: {
  confirmButton: 'btn btn-success',
  cancelButton: 'btn btn-danger'
},
buttonsStyling: false
})
                try {
                    const data = {
                        email : this.email,
                        password : this.password,
                    }
                    const res =  await axios.post('iniciar-sesion',data);
                    this.usuario = res.data;
            
                     localStorage.setItem("getAmosisUser",JSON.stringify(this.usuario));
                     this.getAmosisUser()
                   this.$router.push('/');
                    
                   
                }  catch (error) {
                    
                swalWithBootstrapButtons.fire(
          "Lo sentimos :(",
          "No hemos podido iniciar sesión, intenta de nuevo",
          "error"
        );
                }finally{
                    loader.hide()
                }

            },
           
           
           
        },
        beforeMount() {
            
            },
        mounted() {
             this.$nextTick(async function () {
                            //  let loader = this.$loading.show(LoaderOption);

                  try {
                    
                  }catch (error) {
                  }finally{

                   
                  }
             
        })
   
        },
        updated() {
            
        },
}
</script>
