# FacturarGuias
Proceso de Integración para Facturación de Guías de Despacho

Para realizar el proceso de facturación de guías se pueden aplicar distintas formas, claro que siempre estarán sujetas a dar información de las referencias.

<h3>Facturación Global de Guías</h3>
Este mecanismo se utiliza cuando se quiere facturar masivamente un grupo de guías.
Para se dispone de un "Indicador Global de Facturación", el cual debe ir con valor 1.

En el archivo txt se le deben pasar los parámetros de la siguiente forma:

<pre>
##############################################################                                                 
#######    REFERENCIAS DE FACTURACIÓN GLOBAL DE GUIAS                                                                                
##############################################################
#
# Debe ser 1 para activar el indicado global de facturacion de guias
$doc_referencia["1"]["IndGlobal"]="1";    
#
# Debe ser cero sólo si el documento tiene encendido el Indicador de referencia global.
$doc_referencia["1"]["FolioRef"]="0";                                                  
#
# Tipo de Documento Referenciado 52=GuiaElectronica
$doc_referencia["1"]["TpoDocRef"]="52"; 
#
# Comentario de la Referencia
$doc_referencia["1"]["RazonRef"]="SE FACTURAN GUIAS DEL MES: 3333 - 3334 3337 - 3343";                                                           
#
# El codigo de referencia debe ir vacio
$doc_referencia["1"]["CodRef"]="";
#
# Fecha de de emisión de la factura formato aaaa-mm-dd
$doc_referencia["1"]["FchRef"]="2016-04-28";   
</pre>

Desde el siguiente link podrá ver el formato completo del archivo txt para dicho proceso.
<br>https://github.com/FacTronica/FacturarGuias/blob/master/FormatoFacturaGuiasGlobal.php
