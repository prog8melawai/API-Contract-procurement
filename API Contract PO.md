# po-h object (po-header)
**Note : PO --> Purchase Order**
```
	{
		"po_no": "0000000001",
		"po_date": "17\/05\/2024",
		"pr_no": "0000000003",
		"pr_date": "17\/05\/2024",
		"sup_kd": "A020",
		"netto": 0.0,
		"disc": 0.0,
		"disc_type": "",
		"disc_rp": null,
		"tppn_rp": 0.0,
		"grand_total": 20000.0,
		"crdate": "17\/05\/2024",
		"crtime": "16:38:10",
		"cruser": "ADMIN",
		"upddate": null,
		"upduser": "",
		"f_status": "1",
		"user_batal": "",
		"tgl_batal": null,
		"expired_date": "17\/05\/2024",
		"expected_date": "17\/05\/2024",
		"dept_kd": "FBP",
		"divisi_kd": "11",
		"subdiv_kd": "P",
		"kontrakno": "0000000002",
		"kontrak_date": null,
		"f-complete": false
	}
```

# po-h (po-header) and po-d object (po-detail)
```
{
	"po_no": "0000000001",
	"po_date": "17\/05\/2024",
	"pr_no": "0000000003",
	"pr_date": "17\/05\/2024",
	"sup_kd": "JAYA KENCANA.PT",
	"netto": 0.0,
	"disc": 0.0,
	"disc_type": "",
	"disc_rp": null,
	"tppn_rp": 0.0,
	"grand_total": 20000.0,
	"crdate": "17\/05\/2024",
	"crtime": "16:38:10",
	"cruser": "ADMIN",
	"upddate": null,
	"upduser": "",
	"f_status": "1",
	"user_batal": "",
	"tgl_batal": null,
	"expired_date": "17\/05\/2024",
	"expected_date": "17\/05\/2024",
	"dept_kd": "Food & Beverage Production",
	"divisi_kd": "HOTEL",
	"subdiv_kd": "RUANG MAHA KARYA",
	"kontrakno": "0000000002",
	"kontrak_date": null,
	"f_complete": false,
	"items": [
		{
			"po_no": "0000000001",
			"po_date": "17\/05\/2024",
			"kdbar": "0006",
			"kdjns": "11P10",
			"kdstn_stok": "013",
			"kdstn_krm": "",
			"qty": 2.0,
			"disc_type": "",
			"disc": null,
			"disc_rp": null,
			"ppn": 11.0,
			"ppn_rp": 4400.0,
			"qty_trm": 0.0,
			"lok_kd": "MOVENPICK HOTEL JAKARTA CITY CENTRE",
			"harga": 20000.0,
			"qty_terima": 0.0,
			"kdstn_beli": "003"
		}
	]
}
```