<template>
    
     <section  id="about" class="section">

    <div class="cekongkirr">

    <div class="querypage_box">
        <form>
            <div class="querypage_content" style="overflow: initial">
                <div class="query_nav_list flex">
                    <div class="query_nav_item flex_1" onclick="location.href=&#39;/track&#39;">
                        Trace &amp; Track                    </div>
                    <div class="query_nav_item flex_1 on">
                        Shipping Rates                    </div>
                    <div class="query_nav_item flex_1" onclick="location.href=&#39;/finddroppoint&#39;">
                        Find Drop Point                    </div>
                </div>
                <div class="bjcx_box">
                    <div style="box-shadow: 0 2px 12px 2px #ddd;padding-bottom: 20px;">
                        <div class="bjcx_info_form">

                            <div class="clear_b flex_in min_block">
                                <div class="cx_form_item jjcs_yfcx_select flex_1 on">

                                <label for="cars">Kota Pengirim:</label>
                                    <select  v-model="kotaPengirim">
                                         <option v-for="kpg in kotaPengirimList" :key="kpg.ID" v-bind:value="kpg.ID">{{kpg.CITY_NAME}}</option>
                        
                                    </select>
                            </div>

                            <div class="cx_form_item jjcs_yfcx_select flex_1 on">

                                <label for="cars">Kota Penerima:</label>
                                    <select   v-model="kotaPenerima">
                                         <option v-for="kpr in kotaPenerimaList" :key="kpr.ID" v-bind:value="kpr.ID">{{kpr.CITY_NAME}}</option>
                        
                                    </select>

                            </div>


                            

                            </div>

                            <div class="clear_b flex_in min_block">
                                <div class="cx_form_item jjcs_yfcx_select flex_1 on">
                                    <p>From</p>
                                    <div class="pos_r search_select">
                                        <input type="text" class="cx_form_inp search_input" data-type="1" value="" id="jjcs_search_input">
                                        <div class="search_my_box" style="display: none;">
                                            <!--                                        <input type="text" class="search_keywork" data-type="1" />-->
                                            <div class="search_cont_box">
                                                <div class="search_my_histroy" style="display: block;"><p>Your Search Histroy</p><ul><li class="mysearch_item" data-value="BANDUNG,JAWA?BARAT">BANDUNG,JAWA BARAT</li></ul></div>
                                                <div class="search_my_popular" style="display: block;"><p>Popular Cities</p>
                                                    <ul>
                                                        <li class="mysearch_item" data-value="JAKARTA,DKI JAKARTA">JAKARTA,DKI JAKARTA</li>
                                                        <li class="mysearch_item" data-value="BANDUNG,JAWA BARAT">BANDUNG,JAWA BARAT</li>
                                                        <li class="mysearch_item" data-value="SURABAYA,JAWA TIMUR">SURABAYA,JAWA TIMUR</li>
                                                        <li class="mysearch_item" data-value="YOGYAKARTA,D.I YOGYAKARTA">YOGYAKARTA,D.I YOGYAKARTA</li>
                                                        <li class="mysearch_item" data-value="SEMARANG,JAWA TENGAH">SEMARANG,JAWA TENGAH</li>
                                                    </ul>
                                                </div>
                                                <div class="search_my_keylist" style="display: none;"><ul><li class="mysearch_item" data-value="BANDUNG,JAWA?BARAT"><span class="col_them">BANDUNG,JAWA BARAT</span></li></ul></div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <div class="cx_form_item sjcs_yfcx_select flex_1 on">
                                    <p>To</p>
                                    <div class="pos_r search_select">
                                        <input type="text" class="cx_form_inp search_input" data-type="2" value="" id="sjcs_search_input">
                                        <div class="search_my_box" style="display: none;">
                                            <!--                                        <input type="text" class="search_keywork" data-type="2" />-->
                                            <div class="search_cont_box">
                                                <div class="search_my_histroy" style="display: none;"><p>Your Search Histroy</p><ul><li class="mysearch_item" data-value="WONOKROMO,SURABAYA">WONOKROMO,SURABAYA</li></ul></div>
                                                <div class="search_my_popular" style="display: none;"><p>Popular Cities</p>
                                                    <ul>
                                                        <li class="mysearch_item" data-type="city" data-value="JAKARTA,DKI JAKARTA">JAKARTA,DKI JAKARTA</li>
                                                        <li class="mysearch_item" data-type="city" data-value="BANDUNG,JAWA BARAT">BANDUNG,JAWA BARAT</li>
                                                        <li class="mysearch_item" data-type="city" data-value="SURABAYA,JAWA TIMUR">SURABAYA,JAWA TIMUR</li>
                                                        <li class="mysearch_item" data-type="city" data-value="YOGYAKARTA,D.I YOGYAKARTA">YOGYAKARTA,D.I YOGYAKARTA</li>
                                                        <li class="mysearch_item" data-type="city" data-value="SEMARANG,JAWA TENGAH">SEMARANG,JAWA TENGAH</li>
                                                    </ul>
                                                </div>
                                                <div class="search_my_keylist" style=""><ul><li class="mysearch_item" data-value="WONOKROMO,SURABAYA"><span class="col_them">WONOKROMO,SURABAYA</span></li></ul></div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <div class="cx_form_item cx_zlinput on">
                                    <p>Weight</p>
                                    <input class="cx_form_inp zl_inp" oninput="xzWeight(value)" id="weight" value="" type="number" style="width: 90px;">
                                    <span class="zl_kg">KG</span>
                                    <button type="button" class="query_zl_add col_them" onclick="weightbtn(1)"><img src="./cekongkirjnt_files/add_icon.png"></button>
                                    <button type="button" class="query_zl_reduce col_them" onclick="weightbtn(2)"><img src="./cekongkirjnt_files/reduce_icon.png"></button>
                                </div>
                            </div>
                            <div class="clear_b">
                                <div class="cx_form_item bj_inp on">
                                    <span class="bj_span"><input type="checkbox" class="bj_check">Insurance</span>
                                    <span class="idr_bj" style="display: block;">IDR</span>
                                    <input class="cx_form_inp" style="display: inline-block;" oninput="baojiazh(this.value)" type="tel" placeholder="Please fill in the Item Value">
                                </div>
                                <div class="cx_form_item cc_cont_box">
                                    <span class="bjcx_wycc">
                                        <label>
                                            <input type="checkbox" onchange="ccisshow()" class="bj_checkbox" style="margin-right: 5px">Dimension                                        </label>
                                    </span>
                                    <div class="cx_form_item cc_item" style="">
                                        <div class="flex pos_r">
                                            <div class="cc_inp flex_1">
                                                <input id="loogcm" oninput="DWCalculation()" type="number" :value="30" readonly placeholder="Length">
                                                <span class="cc_cm">CM</span>
                                            </div>
                                            <div class="cc_inp flex_1">
                                                <input id="widthcm" oninput="DWCalculation()" type="number" :value="30" readonly placeholder="Width">
                                                <span class="cc_cm">CM</span>
                                            </div>
                                            <div class="cc_inp flex_1">
                                                <input id="heightcm" oninput="DWCalculation()" type="number"  :value="30" readonly  placeholder="Height">
                                                <span class="cc_cm">CM</span>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <div class="cc_zl" style="">Dimensional Weight: <span class="Calculation">4.5</span>KG</div>
                            </div>
                        </div>
                        <div class="bj_cont_box">
                            <table class="bj_table" cellpadding="0" cellspacing="0" style="visibility: initial;">
                                <thead>
                                <tr>
                                    <th>Service Type</th>
                                    <th>Weight</th>
                                    <th>Shipping Rates</th>
                                    <th>Insurance</th>
                                    <th>Total Fee</th>
                                </tr>
                                </thead>
                                <tbody><tr><td>EZ</td><td>4.5KG</td><td>IDR {{biayaOngkir}}</td><td>IDR 20</td><td class="col_them">IDR {{biayaOngkir}}</td></tr></tbody>
                            </table>
                        </div>


                        
                            <label for="cars">Kota Pengirim:</label>
                            <select  v-model="kotaPengirim">
                            <option v-for="cekOngki in cekOngkir" :key="cekOngki.id" v-bind:value="cekOngki.fkKotaPengirim">{{cekOngki.KotaPengirim.CITY_NAME}}</option>
                   
                            </select>
                            <span>Selected: {{ kotaPengirim }}</span>  <br> 


                          <label for="cars">Kota Penerima:</label>
                            <select   v-model="kotaPenerima">
                            <option v-for="cekOngki in cekOngkir" :key="cekOngki.id" v-bind:value="cekOngki.fkKotaPenerima" >{{cekOngki.KotaPenerima.CITY_NAME}}</option>
                 
                            </select>


                    
                            <span>Selected: {{ kotaPenerima }}</span>   


                
                        <button type="button" class="cx_btn"  v-on:click="oncari()">Search</button>
                    </div>
                </div>
            </div>
            
        </form>

        
    </div>  <!-- end query page box -->
    </div>  <!-- end cekongkirr -->
    

    

    
    <div class="container">
        <div class="row">
       
            
        
        </div>
    </div>

    </section>
</template>




<script>
import axios from 'axios'

    export default {
        
        data(){
            return{
                title:'',
                NomorResi:'',
                datamethods:false,
                cekOngkir:[],
                kotaPengirim:'',
                kotaPenerima:'',
                biayaOngkir:0,
                kotaPengirimList:[],
                kotaPenerimaList:[],


            }
        },

        methods:{
            handleSubmit(){
                // validate password
                this.datamethods=true;
                console.log("form submittd");
                this.oncari();
            },
             async load(){},

            oncari(){


                axios.get(`http://localhost:3011/api/Cekongkirs?filter={"where": {"and": [{"fkKotaPenerima": "${this.kotaPenerima}"}, {"fkKotaPengirim": "${this.kotaPengirim}"}]}}`)
                 .then((response2)=>{
                    console.log("response cekongkir",response2)
                    this.biayaOngkir = response2.data[0].ongkosKirim;
                                        console.log("ongkir",this.biayaOngkir)

                    
                }
                )     
               
            },

            loadCekOngkir(){
                axios.get(`http://localhost:3011/api/Cekongkirs?filter={"include":["KotaPengirim","KotaPenerima"]}`)
                .then((response)=>{
                    console.log("response loadcekongkir",response)
                    this.cekOngkir = response.data;  
                               

                     response.data.forEach(co => {
                         this.kotaPenerimaList.push(
                             co.KotaPenerima
                         )
                         console.log("foraeachco")
                     });

                      this.seenPenerima = new Set();
                
                                this.kotaPenerimaList = this.kotaPenerimaList.filter(el => {
                                  this.duplicatePenerima = this.seenPenerima.has(el.ID);
                                  this.seenPenerima.add(el.ID);
                                  return !this.duplicatePenerima;
                                });

                    // this.kotaPenerimaList = [ ...new Set(this.kotaPenerimaList) ]
                   
                        console.log("kpl", this.kotaPenerimaList)

//---------------------------------------
                       response.data.forEach(co => {
                         this.kotaPengirimList.push(
                             co.KotaPengirim
                         )
                     });

                            this.seenPengirim=  new Set();
                
                                this.kotaPengirimList = this.kotaPengirimList.filter(el => {
                                  this.duplicatePengirim = this.seenPengirim.has(el.ID);
                                  this.seenPengirim.add(el.ID);
                                  return !this.duplicatePengirim;
                                });

                    // thi


                     console.log("kpg", this.kotaPengirimList)


                }
                )     
               

            }

  

        },

        beforeMount(){
            this.loadCekOngkir()
        },
      
   
    }

</script>


<style scoped>


   /* @import './css/style.css'; */
    @import './css/About.css';

    @import './css/animate.css';

    @import './css/Blog-Template.css';

    @import './css/bootstrap.min.css';

    @import './css/etlinefont.css';

    @import './css/font-awesome.css';

    @import './css/magnific-popup.css';
    @import './css/nicepage.css';

    @import './css/Post-Template.css';
</style>