# NIC

<form method="POST">
<div>
<label>NIC</label>
<input name="NIC" type="text" placeholder="NIC number" required autocomplete="off">
</div>
<div>
<button type="submit"  name="Register">Validate</button>
</div>  
</form>

<?php
if (isset($_REQUEST['Register']))
{
$NIC=$_POST['NIC'];
 if(  preg_match('/^([0-9]{9}[x|X|v|V]|[0-9]{12})$/', $NIC))
{
echo "Success";
}
else
{
echo "Failed";
}
?>
