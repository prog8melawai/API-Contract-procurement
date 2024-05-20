# po-h object (po-header)
**Note : PO --> Purchase Order**
```
	{
		"po_no": String,
		"po_date": Date,
		"pr_no": String,
		"pr_date": Date,
		"sup_kd": String,
		"netto": Float,
		"disc": Float,
		"disc_type": String,
		"disc_rp": Float,
		"tppn_rp": Float,
		"grand_total": Float,
		"crdate": Date,
		"crtime": String,
		"cruser": String,
		"upddate": Date,
		"upduser": String,
		"f_status": String,
		"user_batal": String,
		"tgl_batal": Date,
		"expired_date": Date,
		"expected_date": Date,
		"dept_kd": String,
		"divisi_kd": String,
		"subdiv_kd": String,
		"kontrakno": String,
		"kontrak_date": Date,
		"f-complete": Boolean,
		"user-conf" : String,
		"tgl-conf" : Date
	}
```

# po-h (po-header) and po-d object (po-detail)
```
{
	"po_no": String,
	"po_date": Date,
	"pr_no": String,
	"pr_date": Date,
	"sup_kd": String,
	"netto": Float,
	"disc": Float,
	"disc_type": String,
	"disc_rp": Float,
	"tppn_rp": Float,
	"grand_total": Float,
	"crdate": Date,
	"crtime": String,
	"cruser": String,
	"upddate": Date,
	"upduser": String,
	"f_status": String,
	"user_batal": String,
	"tgl_batal": Date,
	"expired_date": Date,
	"expected_date": Date,
	"dept_kd": String,
	"divisi_kd": String,
	"subdiv_kd": String,
	"kontrakno": String,
	"kontrak_date": Date,
	"f-complete": Boolean,
	"user-conf" : String,
	"tgl-conf" : Date
	"items": [
		{
			"po_no": String,
			"po_date": Date,
			"kdbar": String,
			"kdjns": String,
			"kdstn_stok": String,
			"kdstn_krm": String,
			"qty": Float,
			"disc_type": String,
			"disc": Float,
			"disc_rp": Float,
			"ppn": Float,
			"ppn_rp": Float,
			"qty_trm": Float,
			"lok_kd": String,
			"harga": Float,
			"qty_terima": Float,
			"kdstn_beli": String
		}
	]
}
```

**GET /procurement/web//getpo/{{token}}** 
----
  Returns all PO Headers (po-h) in the system
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
        {<po-h object>},
        {<po-h object>},
        {<po-h object>},
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


**GET /procurement/web/getpodetail/{{pono}}/{{token}}** 
----
  Returns PO header and PO detail based on the pono parameter.
* **URL Params**  
  *Required:* `token=[string]`
  *Required:* `pono=[string] (unique)`
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
        {<po-h and po-d object>}
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

