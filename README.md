 <!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
</head>
<body>


<h1>Adi&Ioana</h1>
<p>Introduceti data in care o sa vedeti fluturica</p>
<form action="/action_page.php">
<input type="date" id="bday" min="2018-01-02"><br><br>
<script type="text/javascript">

function myf(){ 
document.getElementById("bday").addEventListener("change", function() {
    var input = this.value;
    var dateEntered = new Date(input);
    var date_diff_indays = function() {
		dt1 = new Date();
		dt2 = new Date(input);
		return Math.floor((Date.UTC(dt2.getFullYear(), dt2.getMonth(), dt2.getDate()) - Date.UTC(dt1.getFullYear(), dt1.getMonth(), dt1.getDate()) ) /(1000 * 60 * 60 * 24));
}
    console.log(date_diff_indays());
    document.getElementById('demo').innerHTML = date_diff_indays();
});
}

</script>

<button type="button"
var input = document.getElementById("bday").value;
onclick="myf()">
Afla cate zile au mai ramas!</button>

<p id="demo"></p>
<p id="bday"></p>
</form>

</body>
</html>  
