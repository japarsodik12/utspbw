## Mahasiswa
<details>
<summary> Klik untuk Ekspan </summary>

### Create Mahasiswa (POST)
<table>
<tr>
 <td><b> URL </b></td>
<td> {{baseURL}}/api/v1/mahasiswa </td>
</tr>
<tr>
<td><b> Method</b> </td>
<td> POST </td>
</tr>
<tr>
<td> <b> Header</b>  </td>
<td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b> Body </b>  </td>
<td>

``` Json
{
    "nama"   : "astri"
    "alamat" : "bekasi"
    "hobi"   : "ngoding"
}
```


<tr>
<td> <b> Respon Succes </b>  </td>
<td>

``` Json
{
    "code" : 201,
    "message" : "Data Mahasiswa Berhasil diinput",
    "data" : {
        "nama"   : "fatur"
        "alamat" : "puncak"
        "hobi"   : "badminton"
    }
}
```
</td>
</tr>
<td> <b> Respon  Conflict </b>  </td>
<td>

``` Json
{
    "code" : 409,
    "message" : "Nama Mahasiswa Telah Digunakan",
    "data" : {
        "nama"   : "andri"
        "alamat" : "ternate"
        "hobi"   : "berenang"
    }
}
```

</td>
</tr>
</table>


### Read Mahasiswa  By id
<table>
<tr>
 <td><b> URL </b></td>
<td> {{baseURL}}/api/v1/mahasiswa </td>
</tr>
<tr>
     <td><b> Example </b></td>
    <td> {{baseURL}}/api/v1/mahasiswa?id=1234 </td>
</tr>
<tr>
    <td><b> Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b> Header</b>  </td>
<td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b> Query </b>  </td>
<td> id=1234 </td>

<tr>
<td> <b> Respon Succes with Query </b>  </td>
<td>

``` Json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : {
        "id"     : 1234,
        "nama"   : "kamil"
        "alamat" : "tasik"
        "hobi"   : "futsal"
    }
}
```
</td>
</tr>
<td> <b> Respon  Conflict </b>  </td>
<td>

``` Json
{
    "code" : 409,
    "message" : "Nama Mahasiswa Telah Digunakan",
    "data" : {
        "nama"   : "mira"
        "alamat" : "banten"
        "hobi"   : "shopping"
    }
}
```

</td>
</tr>
<tr>
<td> <b> Respon  Not Found </b>  </td>
<td>

``` Json
{
    "code" : 404,
    "message" : "ID Mahasiswa Tidak Ditemukan",
    "data" : {
        "value"   : 1234,
        "property" : "id"
        "location"   : "query"
    }
}
```

### Read Mahasiswa All
<table>
<tr>
 <td><b> URL </b></td>
<td> {{baseURL}}/api/v1/mahasiswa </td>
</tr>
<tr>
     <td><b> Example </b></td>
    <td> {{baseURL}}/api/v1/mahasiswa?id=1234 </td>
</tr>
<tr>
    <td><b> Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b> Header</b>  </td>
<td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b> Query </b>  </td>
<td> id=1234 </td>

<tr>
<td> <b> Respon Success </b>  </td>
<td>

``` Json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : [
    {
        "id"     : 1234,
        "nama"   : "rumi"
        "alamat" : "bekasi"
        "hobi"   : "jalan jalan"
    },
    {
    "id" : 1234,
        "nama"   : "susi"
        "alamat" : "jampang"
        "hobi"   : "pelet"
    }
    ]
}
```
</td>
</tr>
<td> <b> Respon  Conflict </b>  </td>
<td>

``` Json
{
    "code" : 409,
    "message" : "Nama Mahasiswa Telah Digunakan",
    "data" : {
        "nama"   : "lina"
        "alamat" : "bogor"
        "hobi"   : "renang"
    }
}
```

</td>
</tr>
<tr>
<td> <b> Respon  Not Found </b>  </td>
<td>

``` Json
{
    "code" : 404,
    "message" : "ID Mahasiswa Tidak Ditemukan",
    "data" : {
        "value"   : 1234,
        "property" : "id"
        "location"   : "query"
    }
}
```
</td>
</tr>
</table>

### Update Mahasiswa 
<table>
<tr>
 <td><b> URL </b></td>
<td> {{baseURL}}/api/v1/mahasiswa </td>
</tr>
<tr>
<td><b> Method</b> </td>
<td> PUT </td>
</tr>
<tr>
<td> <b> Header</b>  </td>
<td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b> Body </b>  </td>
<td>

``` Json
{
    "id" : 1234,
    "nama"   : "shincan"
    "alamat" : "konoha"
    "hobi"   : "Tidur"
}
```


<tr>
<td> <b> Respon Success </b>  </td>
<td>

``` Json
{
    "code" : 201,
    "message" : "Data Mahasiswa Berhasil diubah",
    "data" : {
        "nama"   : "azis"
        "alamat" : "saguling"
        "hobi"   : "badminton"
    }
}
```
</td>
</tr>
<td> <b> Respon  Conflict </b>  </td>
<td>

``` Json
{
    "code" : 409,
    "message" : "Nama Mahasiswa Telah Digunakan",
    "data" : {
        "nama"   : "rima"
        "alamat" : "tasik"
        "hobi"   : "hiking"
    }
}
</td>
</tr>
<td> <b> Respon  Not Found </b>  </td>
<td>
{
    "code" : 404,
    "message" : "ID Mahasiswa Tidak Ditemukan",
    "data" : {
        "value"   : 1234,
        "property" : "id"
        "location"   : "query"
    }
}
```


</td>
</tr>
</table>


### Delete Mahasiswa 
<table>
<tr>
 <td><b> URL </b></td>
<td> {{baseURL}}/api/v1/mahasiswa </td>
</tr>
<tr>
<td><b> Method</b> </td>
<td> DELETE </td>
</tr>
<tr>
<td> <b> Header</b>  </td>
<td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b> Body </b>  </td>
<td>

``` Json
{
    "id" : 1234,
    "nama"   : "One Piece"
    "alamat" : "Lubang"
    "hobi"   : "jalan"
}
```


<tr>
<td> <b> Respon Success </b>  </td>
<td>

``` Json
{
    "code" : 200,
    "message" : "sukses dihapus",
    "data" : []
     
    }
```

</td>
</tr>
<tr>
<td> <b> Respon Not Found </b>  </td>
</table>

## Dosen

### Create Dosen (POST)
	<table>
<tr>
 <td><b> URL </b></td>
<td> {{baseURL}}/api/v1/mahasiswa </td>
</tr>
<tr>
<td><b> Method</b> </td>
<td> POST </td>
</tr>
<tr>
<td> <b> Header</b>  </td>
<td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b> Body </b>  </td>
<td>

``` Json
{
    "status": "success",
    "data": {
        "name": "KEMAL",
        "hobi": "futsal",
        "age": "27",
        "id": 25
    }
}
```

</td>
</tr>
<tr>
<td> <b> Respon Not Found </b>  </td>
</table>


### Read Dosen (GET)
	<table>
<tr>
 <td><b> URL </b></td>
<td> {{baseURL}}/api/v1/dosen </td>
</tr>
<tr>
<td><b> Method</b> </td>
<td> GET </td>
</tr>
<tr>
<td> <b> Header</b>  </td>
<td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b> Body </b>  </td>
<td>

``` Json
{
    "status": "success",
    "data": {
        "name": "Ardiansya",
        "hobi": "futsal",
        "age": "29",
        "id": 26
    }
}
```

</td>
</tr>
<tr>
<td> <b> Respon Not Found </b>  </td>
</table>

### Update Dosen (PUT)
<table>
<tr>
 <td><b> URL </b></td>
<td> {{baseURL}}/api/v1/dosen </td>
</tr>
<tr>
<td><b> Method</b> </td>
<td> PUT </td>
</tr>
<tr>
<td> <b> Header</b>  </td>
<td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b> Body </b>  </td>
<td>

``` Json
{
    "status": "success",
    "data": {
        "name": "Adam",
        "hobi": "Hiking",
        "age": "29",
        "id": 27
    }
}
```

</td>
</tr>
<tr>
<td> <b> successfully </b>  </td>
</table>

### Delete Dosen (DELETE)
<table>
<tr>
 <td><b> URL </b></td>
<td> {{baseURL}}/api/v1/dosen </td>
</tr>
<tr>
<td><b> Method</b> </td>
<td> DELETE </td>
</tr>
<tr>
<td> <b> Header</b>  </td>
<td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b> Body </b>  </td>
<td>

``` Json
{
    "status": "success",
    "Message": "successfully! deleted Records"
}
```

</td>
</tr>
<tr>
<td> <b> successfully </b>  </td>
</table>

