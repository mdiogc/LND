# LND
para lnd


## Apuntes de como hacer un html
```html
<html>
<head>
<title>consulta resultado en web</title>
</head>
<body>
<table border="10">
<tr>
<td>Referencia</td>
<td>Nombre</td>
<td>Pais</td>
</tr>
{
  for $prov in doc("neptuno.xml")//proveedores
  where $prov/PaisProveedor="Francia"
  return
  <tr>
  <td>{$prov/ReferenciaProveedor/text()}</td>
  <td>{$prov/NombreProveedor/text()}</td>
  <td>{$prov/PaisProveedor/text()}</td>
  </tr>
}

</table>

</body> 
</html>  
```