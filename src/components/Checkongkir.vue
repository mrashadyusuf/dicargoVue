<template>
    
<div>
    <head>
     

    <!--[if lt IE 9]>
    <script src="/static/html5shiv.min.js"></script>
    <script src="/static/respond.min.js"></script>
    <![endif]-->

    

            
    



    </head>
<body>




<!-- Global site tag (gtag.js) - Google Analytics -->





                <div class="bjcx_box">
                    <div style="box-shadow: 0 2px 12px 2px #ddd;padding-bottom: 20px;">
                        <div class="bjcx_info_form">
                            <div class="clear_b flex_in min_block">
                                <div class="cx_form_item jjcs_yfcx_select flex_1 on">
                                    <p>From</p>
                                    <div class="pos_r search_select">
                                        <input type="text" class="cx_form_inp search_input" data-type="1" value="" id="jjcs_search_input">
                                        <div class="search_my_box" style="display: none;">
                                            <!--                                        <input type="text" class="search_keywork" data-type="1" />-->
                                            <div class="search_cont_box">
                                                <div class="search_my_histroy" style="display: block;"><p>Your Search Histroy</p><ul><li class="mysearch_item" data-value="JAKARTA,DKI?JAKARTA">JAKARTA,DKI JAKARTA</li></ul></div>
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
                                                <div class="search_my_histroy" style="display: block;"><p>Your Search Histroy</p><ul></ul></div>
                                                <div class="search_my_popular" style="display: block;"><p>Popular Cities</p>
                                                    <ul>
                                                        <li class="mysearch_item" data-type="city" data-value="JAKARTA,DKI JAKARTA">JAKARTA,DKI JAKARTA</li>
                                                        <li class="mysearch_item" data-type="city" data-value="BANDUNG,JAWA BARAT">BANDUNG,JAWA BARAT</li>
                                                        <li class="mysearch_item" data-type="city" data-value="SURABAYA,JAWA TIMUR">SURABAYA,JAWA TIMUR</li>
                                                        <li class="mysearch_item" data-type="city" data-value="YOGYAKARTA,D.I YOGYAKARTA">YOGYAKARTA,D.I YOGYAKARTA</li>
                                                        <li class="mysearch_item" data-type="city" data-value="SEMARANG,JAWA TENGAH">SEMARANG,JAWA TENGAH</li>
                                                    </ul>
                                                </div>
                                                <div class="search_my_keylist" style="display: none;"><ul><li class="mysearch_item" data-value="WONOKROMO,SURABAYA"><span class="col_them">WONOKROMO,SURABAYA</span></li></ul></div>
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
                                    <span class="idr_bj" style="">IDR</span>
                                    <input class="cx_form_inp" style="" oninput="baojiazh(this.value)" type="tel" placeholder="Please fill in the Item Value">
                                </div>
                                <div class="cx_form_item cc_cont_box">
                                    <span class="bjcx_wycc">
                                        <label>
                                            <input type="checkbox" onchange="ccisshow()" class="bj_checkbox" style="margin-right: 5px">Dimension                                        </label>
                                    </span>
                                    <div class="cx_form_item cc_item" style="">
                                        <div class="flex pos_r">
                                            <div class="cc_inp flex_1">
                                                <input id="loogcm" oninput="DWCalculation()" type="number" value="" placeholder="Length">
                                                <span class="cc_cm">CM</span>
                                            </div>
                                            <div class="cc_inp flex_1">
                                                <input id="widthcm" oninput="DWCalculation()" type="number" value="" placeholder="Width">
                                                <span class="cc_cm">CM</span>
                                            </div>
                                            <div class="cc_inp flex_1">
                                                <input id="heightcm" oninput="DWCalculation()" type="number" value="" placeholder="Height">
                                                <span class="cc_cm">CM</span>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <div class="cc_zl" style="">Dimensional Weight: <span class="Calculation">0</span>KG</div>
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
                                <tbody><tr><td>EZ</td><td>4.5KG</td><td>IDR 95.000</td><td>IDR 200</td><td class="col_them">IDR 95.200</td></tr></tbody>
                            </table>
                        </div>
                        <button type="button" class="cx_btn" onclick="searchQuery()">Search</button>
                    </div>
                </div>         <!-- end bjcx_box -->

<!--<script src="https://www.google.com/recaptcha/api.js" async defer></script>-->

<!-- ///////////////////////////////// -->




</body>
</div>


</template>    




    <style>

      @import './cekongkirjnt_files/jtcss.css';
      @import './cekongkirjnt_files/boots.css';


            html,body,.content_box{
                height: auto;
                background-color: #f5f5f5;
                overflow-y: inherit;
                overflow-x: hidden;
            }
            .bjcx_info_form *{
                box-sizing: border-box;
            }
            .select2-container--default .select2-selection--single{
                font-size: 14px;
                border: 0;
                border-bottom: 2px solid #888;
                width: 318px;
                line-height: 28px;
                -webkit-box-sizing: border-box;
                -moz-box-sizing: border-box;
                box-sizing: border-box;
                border-radius: 0;
            }
            .searchable-select-items{
                max-height: 200px;
            }
            .orderpage_tip{
                left: 0;
            }
        </style>

        <script>
 
 
</script>




