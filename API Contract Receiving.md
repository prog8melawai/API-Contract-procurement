# receiving-h object (receiving-header)

```
{
    "no_karcis": String (30 karakter),
    "tgl_karcis": Date (DD/MM/YYYY),
    "no_sj": String (20 karakter),
    "tgl_sj": Date (DD/MM/YYYY),
    "sup_kd": String (8 karakter),
    "group_type": String (1 karakter),
    "divisi_kd": String (3 karakter),
    "subdiv_kd": String (3 karakter),
    "dept_kd": String (3 karakter),
    "lok_kd": String (5 karakter),
    "netto": Float,
    "disc": Array of objects[
        {
            "disc": Float
        },
    ],
    "f_disc": Array[
        {
            "f_disc": Boolean
        },
    ],
    "disc_rp": Float,
    "ppn": Float,
    "ppn_rp": Float,
    "gtotal": Float,
    "crc_code": String (8 karakter),
    "kd_purch": String (5 karakter),
    "user_entry_rcv": String (15 karakter),
    "tgl_entry_rcv": Date (DD/MM/YYYY),
    "user_confirm_rcv": String (15 karakter),
    "tgl_confirm_rcv": Date (DD/MM/YYYY),
    "user_confirm_byr": String (15 karakter),
    "tgl_confirm_byr": Date (DD/MM/YYYY),
    "cara_bayar": String (1 karakter),
    "f_lengkap": Boolean,
    "f_match": Boolean,
    "f_match_ppn": Boolean,
    "tt_no": String (9 karakter),
    "tt_tgl": Date (DD/MM/YYYY),
    "tt_no_ppn": String (9 karakter),
    "tt_tgl_ppn":  Date (DD/MM/YYYY),
    "due_day": Integer,
    "iv_no":  String (12 karakter),
    "iv_tgl": Date (DD/MM/YYYY),
    "iv_no_ppn": String (12 karakter),
    "iv_tgl_ppn": Date (DD/MM/YYYY),
    "no_kontrak": String (30 karakter),
    "tgl_load": Date (DD/MM/YYYY),
    "tgl_lengkap": Date (DD/MM/YYYY),
    "user_lengkap": String (15 karakter),
    "statusacc": String (50 karakter),
    "rate_beli": Float,
}
```

# receiving-h (receiving-header) and receiving-d (receiving-detail) object
```
{
    "no_karcis": String (30 karakter),
    "tgl_karcis": Date (DD/MM/YYYY),
    "no_sj": String (20 karakter),
    "tgl_sj": Date (DD/MM/YYYY),
    "sup_kd": String (8 karakter),
    "group_type": String (1 karakter),
    "divisi_kd": String (3 karakter),
    "subdiv_kd": String (3 karakter),
    "dept_kd": String (3 karakter),
    "lok_kd": String (5 karakter),
    "netto": Float,
    "disc": Float
    "f_disc": Boolean,
    "disc_rp": Float,
    "ppn": Float,
    "ppn_rp": Float,
    "gtotal": Float,
    "crc_code": String (8 karakter),
    "kd_purch": String (5 karakter),
    "user_entry_rcv": String (15 karakter),
    "tgl_entry_rcv": Date (DD/MM/YYYY),
    "user_confirm_rcv": String (15 karakter),
    "tgl_confirm_rcv": Date (DD/MM/YYYY),
    "user_confirm_byr": String (15 karakter),
    "tgl_confirm_byr": Date (DD/MM/YYYY),
    "cara_bayar": String (1 karakter),
    "f_lengkap": Boolean,
    "f_match": Boolean,
    "f_match_ppn": Boolean,
    "tt_no": String (9 karakter),
    "tt_tgl": Date (DD/MM/YYYY),
    "tt_no_ppn": String (9 karakter),
    "tt_tgl_ppn":  Date (DD/MM/YYYY),
    "due_day": Integer,
    "iv_no":  String (12 karakter),
    "iv_tgl": Date (DD/MM/YYYY),
    "iv_no_ppn": String (12 karakter),
    "iv_tgl_ppn": Date (DD/MM/YYYY),
    "no_kontrak": String (30 karakter),
    "tgl_load": Date (DD/MM/YYYY),
    "tgl_lengkap": Date (DD/MM/YYYY),
    "user_lengkap": String (15 karakter),
    "statusacc": String (50 karakter),
    "rate_beli": Float,
    "items": [
        {
        "group_type":  String (1 karakter),
        "no_karcis": String (30 karakter),
        "tgl_karcis": Date (DD/MM/YYYY),
        "no_po": String (20 karakter),
        "tgl_po": Date (DD/MM/YYYY),
        "dept_kd": String,
        "divisi_kd" : String,
        "subdiv_kd" : String,
        "lok_kd" : String,
        "sup_kd" : String,
        "kd_barang" : String,
        "nm_barang" : String,
        "due_day": Integer,
        "qty": Float,
        "qty_bonus": Float,
        "harga": Float,
        "satuan": String,
        "konversi": Float,
        "uom": String,
        "sub_total": Float,
        "disc": Float,
        "f_disc": Boolean,
        "disc_rp": Float,
        "ppn_bm": Float,
        "ppn_bm_rp": Float,
        "gtotal": Float,
        "harga_po": Float,
        "kd_jenis": String,
        "acc_no": String,
        "pos_budget_kd": String,
        "kd_jenis_old": String,
        "alasan_beda_harga": String,
        "user_cek_harga": String,
        "tgl_cek_harga":Date (DD/MM/YYYY),
        "statusacc": String
        }
    ]
}
```


**GET /procurement/web/receiving/{{token}}** 
----
  Returns all Receiving Headers (receiving-h) in the system
* **URL Params**  
  *Required:* `token=[string]`
* **Data Params**  
  None
* **Headers**  
  Content-Type: application/json
* **Success Response:**  
* **Code:** 200  
  **Content:**  
```
{
    [
        {<receiving-h object>},
        {<receiving-h object>},
        {<receiving-h object>},
        ....
    ]
}
```

* **Error Response:**  
  * **Code:** 404  
  **Content:** `{ error : "Unauthorized" }`  
  OR  
  * **Code:** 401  
  **Content:** `{ error : "Unauthorized" }`  
  OR 
  * **Code:** 503  
  **Content:** `{ error : "Database not connected" }`  

**GET /procurement/web/receiving/{{nokarcis}}/{{token}}** 
----
  Returns Receiving header and detail based on the nokarcis parameter.
* **URL Params**  
  *Required:* `token=[string]`
  *Required:* `nokarcis=[string] (unique)`
* **Data Params**  
  None
* **Headers**  
  Content-Type: application/json
* **Success Response:**  
* **Code:** 200  
  **Content:**  
```
{
    [
        {<receiving-h and receiving-d object>}
    ]
}
```

* **Error Response:**  
  * **Code:** 404  
  **Content:** `{ error : "Unauthorized" }`  
  OR  
  * **Code:** 401  
  **Content:** `{ error : "Unauthorized" }`  
  OR 
  * **Code:** 503  
  **Content:** `{ error : "Database not connected" }`  


**POST /procurement/web/receiving/{{token}}** 
----
Creates new receiving header with details, returns success message.
No karcis is automatically generated by increment counter and ignores the no_karcis variable set in body.
* **URL Params**  
  *Required:* `token=[string]`
* **Data Params**  
    {
        {<receiving-h and receiving-d object>}
    }
* **Headers**  
  Content-Type: application/json
* **Success Response:**  
* **Code:** 200  
  **Content:**  
```
{
	"message": "receiving note created successfully!"
}
```

* **Error Response:**  
  * **Code:** 404  
  **Content:** `{ error : "Unauthorized" }`  
  OR  
  * **Code:** 401  
  **Content:** `{ error : "Unauthorized" }`  
  OR 
  * **Code:** 503  
  **Content:** `{ error : "Database not connected" }`  

  **PUT /procurement/web/updatereceiving/{{nokarcis}}/{{token}}**
  Updates Receiving-Detail fields on the specified nokarcis Header.
  Can only change the 'qty' field on receiving-d of the specified nokarcis.
* **URL Params**  
  *Required:* `token=[string]`
  *Required:* `nokarcis=[string] (unique)`
* **Data Params**  
    {
      "items": [
				{
					"qty": Float
				}
			]
}
* **Headers**  
  Content-Type: application/json
* **Success Response:**  
* **Code:** 200  
  **Content:**  
```
{
	"message": "Receiving Quantity Revised successfully!"
}
```

* **Error Response:**  
  * **Code:** 404  
  **Content:** `{ error : "Unauthorized" }`  
  OR  
  * **Code:** 401  
  **Content:** `{ error : "Unauthorized" }`  
  OR 
  * **Code:** 503  
  **Content:** `{ error : "Database not connected" }`  